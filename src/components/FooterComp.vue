<template>

    <footer>
        <!-- subscribe section -->
        <div id="top-foot" class="container">
            <div class="input-group mb-3">
                <input type="text" class="form-control my-custom-width" placeholder="Subscribe to our newsletter">
                <div class="input-group-append">
                    <button class="btn btn-outline-secondary my-radius" type="button" id="button-addon2">Register</button>
                </div>
            </div>
            <div>
                <p><a href="#">Insights is Picwik</a> University's thought leadership publication for sharing knowlege on management, technology and innovation.</p>
                <span><a href="#">Take me there</a></span>
            </div>
        </div>

        <!-- contact us section -->
        <div id="mid-foot" class="container">
            <ul v-for="list in footerExplore" :key="list.id"> 
                <h3>{{ list.title }} </h3>
                <li v-for="item in list.items" :key="item.id">{{ item.content }}</li>
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
                footerExplore:[
                    {   
                        id: 1,
                        title: 'Contact Us',
                        items: [
                            {
                                content: '900 Wood Street, MI New York 48607'
                            },
                            {
                                content: '+56 345 678 000-09'
                            },
                            {
                                content: 'info@example.com'
                            }
                        ]
                    },
                    {   
                        id: 2,
                        title: 'Support Us',
                        items: [
                            {
                                content: 'Privacy'
                            },
                            {
                                content: 'Terms'
                            },
                            {
                                content: 'Cookie Policy'
                            },
                            {
                                content: 'Sitemap'
                            }
                        ]
                    },
                    {
                        id: 3,
                        title: 'Explore',
                        items: [
                            {
                                content: 'Accomodation'
                            },
                            {
                                content: 'Arts Academics'
                            },
                            {
                                content: 'Central Services'
                            },
                            {
                                content: 'Conferences and Events'
                            },
                            {
                                content: 'Food and Drink'
                            }
                        ]
                    },
                    {
                        id: 4,
                        title: 'Visit',
                        items: [
                            {
                                content: 'Admission'
                            },
                            {
                                content: 'Contact Us'
                            },
                            {
                                content: 'FAQs'
                            },
                            {
                                content: 'Request Information'
                            },
                            {
                                content: 'Privacy Notice'
                            }
                        ]
                    }
                ]
            }
        }
     }
</script>

<style lang="scss" scoped>
    .my-custom-width{
        max-width: 25%;
    }
    .my-radius{
        border-radius: 0;
    }
</style>