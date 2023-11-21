<template>

    <footer>
        <!-- subscribe section -->
        <div id="top-foot" class="container">
            <div>
                <div class="input-group mb-3 d-flex">
                    <input type="text" class="form-control w-25 " placeholder="Subscribe to our newsletter">
                    <div class="input-group-append">
                        <button class="btn btn-outline-secondary" type="button" id="button-addon2">Register</button>
                    </div>
                </div>
            </div>
            <div>
                <p><a href="#">Insights is Picwik</a> University's thought leadership publication for sharing knowlege on management, technology and innovation.</p>
                <span><a href="#">Take me there</a></span>
            </div>
        </div>

        <!-- contact us section -->
        <div id="mid-foot" class="container">
            <h3>{{ title }}</h3>
            <ul>
                <li v-for="contact in contactUs" :key="contact.id">{{ contact }}</li>
            </ul>
        </div>

        <!-- copyright section -->
        <div id="bottom-foot" class="container">

        </div>
    </footer>
    
</template>

<script>
    export default {
        name: 'FooterComp',
        data() {
            return {
                contactUs:
                    {
                        title: 'Contact Us',
                        address: '900 Wood Street, MI New York 48607',
                        phoneNum: '+56 345 678 000-09',
                        email: 'info@example.com'
                    },
                    explore: [
                        
                    ]
                }
            }
        }
</script>

<style lang="scss" scoped>

</style>