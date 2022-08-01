    <template>
    <div>
        <nav class="flex items-center justify-between flex-wrap bg-blue-700 p-6">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
            <span class="font-semibold text-xl tracking-tight">Welcome!!</span>
        </div>
        <!-- <div class="flex justify-endinline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-teal-500 hover:bg-white mt-4 lg:mt-0">
            <nuxt-link
            v-if="authenticated"
            to="/index"
            @click="logout"
            replace
            >LogOut</nuxt-link
            >
            </div> -->
            <button type="button " class="flex justify-endinline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-teal-500 hover:bg-white mt-4 lg:mt-0">LogOut</button>
        <router-view @authenticated="setAuthenticated" />
        </nav>
        <div class="grid grid-cols-3 gap-5 mt-14">
        <div
            class="p-6 max-w-sm bg-red-800 rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:border-gray-700"
        >
            <a href="#">
            <h5
                class="mb-2 text-2xl text-center font-bold tracking-tight text-gray-900 dark:text-white"
            >
                Apple
            </h5>
            </a>

            <div class="flex flex-1 justify-center p-9 text-4xl">10</div>

            <div class="flex flex-1 justify-center">
            <button
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="increment"
            >
                +
            </button>
            <button
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="decrement"
            >
                -
            </button>
            </div>
        </div>
        <div
            class="p-6 max-w-sm bg-yellow-500 rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:border-gray-700"
        >
            <a href="#">
            <h5
                class="mb-2 text-2xl text-center font-bold tracking-tight text-gray-900 dark:text-white"
            >
                Orange
            </h5>
            </a>

            <div class="flex flex-1 justify-center p-9 text-4xl">10</div>

            <div class="flex flex-1 justify-center">
            <button
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="increment"
            >
                +
            </button>
            <button
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="decrement"
            >
                -
            </button>
            </div>
        </div>
        <div
            class="p-6 max-w-sm bg-blue-500 rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:border-gray-700"
        >
            <a href="#">
            <h5
                class="mb-2 text-2xl text-center font-bold tracking-tight text-gray-900 dark:text-white"
            >
                Grapes
            </h5>
            </a>

            <div class="flex flex-1 justify-center p-9 text-4xl">10</div>

            <div class="flex flex-1 justify-center">
            <button
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="increment"
            >
                +
            </button>
            <button
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="decrement"
            >
                -
            </button>
            </div>
        </div>
        </div>

        <!-- <div class="grid grid-flow-col text-center p-2"> 
        <div class="shadow-sm w-80 h-24 bg-green-200 
                    rounded-lg">shadow-sm
        </div>
        </div> -->
    <div class="flex justify-center items-center min-w-0 bg-white">
        
        <div class="flex-1 max-w-4xl p-16">
            <h2 class="text-center p-10 font-bold">Basket Stack</h2>
            <div class="col-span-2 text-center text-white p-4 pr-6 bg-orange-500 border-1-8 border-teal-400 rounded-md shadow-md space-y-2">
            Orange
        </div>
        <div class="col-span-2 text-center text-white p-4 pr-6 bg-red-500 border-1-8 border-teal-400 rounded-md shadow-md space-y-2">
            Apple
        </div>
        <div class="col-span-2 text-center text-white p-4 pr-6 bg-blue-500 border-1-8 border-teal-400 rounded-md shadow-md space-y-2">
            Grape
        </div>
        </div>
    </div>

        
    </div>
    </template>

    <!-- // const count=ref(0)
        // const plusOne=computed(()=>count.value + 1)
        // function decrement(){
        //     count.value--
        // }
        // function increment(){
        //     count.value++
        // } -->

    <script>
    // import('@vue/reactivity').ComputedRef();
    const count=ref(0)
    const plusOne=computed(()=>count.value + 1)
    export default {
    name: "App",
    data() {
        return {
        authenticated: false,
        mockAccount: {
            username: "madhuri",
            password: "password",
            count: ref(0),
        },
        };
    },
    mounted() {
        if (!this.authenticated) {
        this.$router.replace({ name: "login" });
        }
    },
    methods: {
        setAuthenticated(status) {
        this.authenticated = status;
        },
        logout() {
        this.authenticated = false;
        },
        decrement(){
            count.value--
        },
        increment(){
            count.value++
        },
        
    },
    };
    </script>
