


     <template>
         <div class="flex items-center justify-center min-h-screen bg-gray-100">
        <div class="px-8 py-6 mt-4 text-left bg-white shadow-lg">
                <p class="text-2xl font-bold m-5 ">
                Login
                </p>
    
                <form action="components/card.vue" method="post">
                    <input v-model="input.username" aria-label="Enter your email address" 
                        type="text" placeholder="User Name" 
                        class="text-sm text-gray-base w-full 
                                mr-3 py-5 px-4 h-2 border 
                                border-gray-200 rounded mb-2" />
                    <input v-model="input.password" aria-label="Enter your password" 
                        type="password" placeholder="Password"
                        class="text-sm text-gray-base w-full mr-3 
                                py-5 px-4 h-2 border border-gray-200 
                                rounded mb-2" />
                <div class="flex justify-center">
                    <!-- <NaxtLink v-on:click="login()"
                        class="shadow bg-purple-500 hover:bg-purple-400 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-4 rounded"
                        type="button"
                        >
                        Submit -->
                        <button type="button" @click="login" class="shadow bg-purple-500 hover:bg-purple-400 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-4 rounded"
                        >Submit</button>
                </div>
        
                </form>
            </div>
            </div>
            <Card/>
    </template>

    <!-- <script>
// import { sign } from 'crypto';
 import axios from "axios"
export default{
    name:"sign",
    data()
    {
        return {
            name:'',
            email:'',
            password:'',
        }
    },
    methods:{
        async sign(){
            console.warn("this is called",this.name,this.password)
            let result= await axios.post("http://localhost:3000/users",{
                name:this.name,
                password:this.password
            })
            console.warn(result);
            if(result.status==201){
                alert("sign up done");
            }
}
    }
}
</script> -->
<script>
export default {
        name: 'Login',
        data() {
            return {
                input: {
                    username: "",
                    password: ""
                }
            }
        },
        methods: {
            login() {
                if(this.input.username != "" && this.input.password != "") {
                    if(this.input.username == this.$parent.mockAccount.username && this.input.password == this.$parent.mockAccount.password) {
                        this.$emit("authenticated", true);
                        this.$router.replace({ name: "secure" });
                    } else {
                        console.log("The username and / or password is incorrect");
                    }
                } else {
                    console.log("A username and password must be present");
                }
            }
        }
    }
</script>