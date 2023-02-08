<template lang="">
<div>
    <!-- <h1>timeout</h1> -->
    {{message}}
    {{data}}
</div>
</template>

<script>
export default {
    data() {
        return {
            // message: "Welcome, Please Wait...."
            message: "",
            data:'',
        }
    },
    methods: {
        
        callFunction: function () {
            var v = this;           
            setTimeout(function () {

                // v.message = "Hi Bro, SetTimeout is working fine.";
                v.message = "Welcome";

            }, 3000);

        },
        callFunction2: function () {
            var p = this;           
            setTimeout(function () {

                // v.message = "Hi Bro, SetTimeout is working fine.";
                p.data = "Bye Bye";

            }, 2000);

        }
    },
    // beforeMount(){
    //     this.callFunction()
    //     // alert("beforemount called")
    //     console.log("beforemount called");
    // },
    mounted() {

        this.callFunction()
        
        console.log("mount called");
    },
    unmounted(){
        this.callFunction2()
        console.log("unmounted");
    }
}
</script>

<style lang="">

</style>
