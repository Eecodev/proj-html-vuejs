<template>

    <footer>
        <!-- subscribe section -->
        <div class="bg-top-mid-foot">
           <div id="top-foot" class="container d-flex justify-content-center align-items-center p-4 border flex-wrap">
                <div class="form-group d-flex align-items-center md-4">
                    <input type="email" class="form-control my-custom-width my-radius mr-2" placeholder="Subscribe to our newsletter">
                    <button class="btn btn-primary my-radius red-btn">Subscribe</button>
                </div>
                <div>
                   <p class="mb-0 p-4">
                        <a href="#" class="red-text">Insights is Picwik</a>
                            University's thought leadership publication for sharing knowledge on management, technology, and innovation.
                        <span class="d-block"><a href="#">Take me there</a></span>
                    </p> 
                </div>
            </div>

        <!-- contact us section -->

            <div id="mid-foot" class="container d-flex align-items-center justify-content-between pt-5 pb-5">
                <ul v-for="list in footerExplore" :key="list.id"> 
                    <h3>{{ list.title }} </h3>
                    <li v-for="item in list.items" :key="item.id">{{ item.content }}</li>
                </ul>
            </div>
            
            
        </div>
        

        <!-- copyright section -->

        <div class="bg-bottom-foot">
            <div id="bottom-foot" class="container d-flex justify-content-between align-items-center">
                <p>Copyright 2020 tophive. All rights Reserved</p>
                <ul class="d-flex">
                    <li class="m-2" v-for="copyright in copyRights" :key="copyright.id">{{ copyright }}</li>
                </ul>
            </div>
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
                ],
                copyRights:[
                    'Privacy',
                    'Terms',
                    'Cookie Policy',
                    'Sitemap'
                ]
            }
        }
     }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

    footer{
        color: $bg-light;
    }
    .bg-top-mid-foot{
        height: 500px;
        background-color: $bg-footer;
    }
    .red-text{
        color: $bg-red;
    }
    .red-btn{
        background-color: $bg-red;
        border: 1px solid $bg-red;
    }
    .bg-bottom-foot{
        background-color: $bg-copyright;
    }
    .my-custom-width{
        width: 250px;
    }
    .my-radius{
        border-radius: 0;
    }
    ul{
        list-style: none;
    }
</style>