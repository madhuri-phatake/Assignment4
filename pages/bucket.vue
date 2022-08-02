    <template>
    <div>
        <!-- <nav class="flex items-center justify-between flex-wrap bg-blue-700 p-6">
            <div class="flex items-center flex-shrink-0 text-white mr-6">
                <span class="font-semibold text-xl tracking-tight">Welcome!!</span>
            </div>
        
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

                <div class="flex flex-1 justify-center p-9 text-4xl">{{plusOne}}</div>

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

                <div class="flex flex-1 justify-center p-9 text-4xl">{{plusoneone}}</div>

                <div class="flex flex-1 justify-center">
                <button
                    class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                    @click="incrementone"
                >
                    +
                </button>
                <button
                    class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                    @click="decrementone"
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

                <div class="flex flex-1 justify-center p-9 text-4xl">{{plusoneotwo}}</div>

                <div class="flex flex-1 justify-center">
                <button
                    class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                    @click="incrementtwo"
                >
                    +
                </button>
                <button
                    class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                    @click="decrementtwo"
                >
                    -
                </button>
                </div>
            </div>
            </div> -->

        <nav class="flex items-center justify-between flex-wrap bg-blue-700 p-6">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
            <span class="font-semibold text-xl tracking-tight">Welcome!!</span>
        </div>
        <div>
            <NuxtLink
            to="/"
            class="flex justify-endinline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-teal-500 hover:bg-white mt-4 lg:mt-0"
            >LogOut</NuxtLink>
            
        </div>
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
            <div class="flex flex-1 justify-center p-9 text-4xl">{{ plusOne }}</div>
            <div class="flex flex-1 justify-center">
            <button
                v-on:click="add"
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="increment"
            >
                +
            </button>
            <button
                v-on:click="remove"
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
            <div class="flex flex-1 justify-center p-9 text-4xl">
            {{ plusoneone }}
            </div>
            <div class="flex flex-1 justify-center">
            <button
                v-on:click="add1"
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="incrementone"
            >
                +
            </button>
            <button
                v-on:click="remove1"
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="decrementone"
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
            <div class="flex flex-1 justify-center p-9 text-4xl">
            {{ plusoneotwo }}
            </div>
            <div class="flex flex-1 justify-center">
            <button
                v-on:click="remove1"
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="incrementtwo"
            >
                +
            </button>
            <button
                v-on:click="remove2"
                class="py-2 px-4 rounded-full h-14 w-14 bg-white text-black mx-1"
                @click="decrementtwo"
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
            <div
            class="col-span-2 text-center text-white p-4 pr-6 bg-orange-500 border-1-8 border-teal-400 rounded-md shadow-md space-y-2"
            >
            {{ basket }} Orange
            </div>
            <div
            class="col-span-2 text-center text-white p-4 pr-6 bg-red-500 border-1-8 border-teal-400 rounded-md shadow-md space-y-2"
            >
            {{ basket }} Apple
            </div>
            <div
            class="col-span-2 text-center text-white p-4 pr-6 bg-blue-500 border-1-8 border-teal-400 rounded-md shadow-md space-y-2"
            >
            {{ basket }} Grape
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

    <!-- // import('@vue/reactivity').ComputedRef();
        // const count=ref(0)
        // const plusOne=computed(()=>count.value + 1)
        // export default {
        // name: "App",
        // data() {
        //     return {
        //     authenticated: false,
        //     mockAccount: {
        //         username: "madhuri",
        //         password: "password",
        //         count: ref(0),
        //     },
        //     };
        // },
        // mounted() {
        //     if (!this.authenticated) {
        //     this.$router.replace({ name: "login" });
        //     }
        // },
        // methods: {
        //     setAuthenticated(status) {
        //     this.authenticated = status;
        //     },
        //     logout() {
        //     this.authenticated = false;
        //     },
        //     decrement(){
        //         count.value--
        //     },
        //     increment(){
        //         count.value++
        //     },
            
        // },
        // };
        // </script> -->
    <script>
    import { remove } from "@vue/shared";
    export default {
    data() {
        return {
        counter: 0,
        orangecounter: 0,
        grapecounter: 0,
        basket: [],
        };
    },
    methods: {
        add() {
        this.counter = this.counter === 10 ? 10 : this.counter + 1;
        this.basket.push("Apple");
        },
        remove() {
        this.counter = this.counter === 0 ? 0 : this.counter - 1;
        let basket = basket.slice(0, -1);
        },
        add1() {
        this.orangecounter =
            this.orangecounter === 10 ? 10 : this.orangecounter + 1;
        this.basket.push("Orange");
        },
        remove1() {
        this.orangecounter =
            this.orangecounter === 0 ? 0 : this.orangecounter - 1;
        basket.splice(-1);
        },
        add2() {
        this.grapecounter = this.grapecounter === 10 ? 10 : this.grapecounter + 1;
        this.basket.push("Grape");
        },
        remove2() {
        this.grapecounter = this.grapecounter === 0 ? 0 : this.grapecounter - 1;
        let basket = basket.splice(-1);
        },
    },
    };
    </script>
