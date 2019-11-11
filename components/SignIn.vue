<template>
    <div className='sign-in'>
        <h2>I already have an account</h2>
        <span>Sign in with your email and password</span>

        <form @submit.prevent="handleSubmit">
            <FormInput 
                name="email" 
                type="email" 
                :value="state.email" 
                @handleChange="handleChange"
                label="email"
                required />
            <FormInput 
                name="password" 
                type="password" 
                :value="state.password" 
                @handleChange="handleChange"
                label="password"
                required/>

            <CustomButton type="submit">Sign in</CustomButton>
        </form>
    </div>
</template>

<script>
import FormInput from './FormInput.vue';
import CustomButton from './CustomButton.vue';

export default {
    components: {
        FormInput,
        CustomButton
    },
    data() {
        return {
            state: {
                email: "",
                password: ""
            }
        };
    },
    methods: {
        handleChange(event) {
            const { value, name } = event.target;
       
            this.$set(this.state, name, value);
        },
        handleSubmit(event) {
            this.$set(this.state, "email", "");
            this.$set(this.state, "password", "");
            this.$forceUpdate();
        }
    }

}
</script>

<style>

</style>