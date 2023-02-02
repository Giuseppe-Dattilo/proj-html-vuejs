<script>
import AppButton from '../generics/AppButton.vue';
import { footerLinks } from '../../data/footerLinks';
export default {
    name: 'AppFooter',
    components: { AppButton },
    data() {
        return {
            footerLinks
        }
    }
}
</script>

<template>

    <!-- Footer-top -->
    <footer>
        <div class="container px-4">
            <div class="row row-cols-4">

                <!-- Address -->
                <div class="bookings">
                    <h5 role="button">BOOKINGS</h5>
                    <address>502 New Design Str,<br>Melbourne, San Francisco, <br>CA 94110, United States Of
                        <br>America
                        Australia
                        <div class="mt-1">T: 1123-456-789</div>
                        <span>Email: </span><a href="#">demo@example.com</a>
                    </address>

                    <!-- Social -->
                    <div class="icon">
                        <ul class="p-1">
                            <li>
                                <a href="#"><img src="../../assets/img/image (17).svg" alt="instagram"></a>
                                <a href="#"><img src="../../assets/img/image (18).svg" alt="instagram"></a>
                                <a href="#"><img src="../../assets/img/image (19).svg" alt="instagram"></a>
                                <a href="#"><img src="../../assets/img/image (20).svg" alt="instagram"></a>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Nav -->
                <nav v-for="(menu, i) in footerLinks.menus" :key="i">
                    <h5 role="button">{{ menu.title }}</h5>
                    <ul class="p-0">
                        <li v-for="(link, i) in menu.links" :key="i"><a href="#">{{ link }}</a></li>
                    </ul>
                </nav>

                <!-- Newsletter-->
                <div class="newsletter">
                    <h5 role="button">NEWSLETTER</h5>
                    <app-button :buttonLabel="'SEND MESSAGE'"></app-button>
                </div>
            </div>
        </div>
    </footer>

    <!-- Footer-bottom -->
    <div class="line"></div>
    <div class="footer-bottom">
        <p class="text-center">&#169; 2023 All Right Reserved. Developed By TemplateMela</p>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

footer {
    min-height: 400px;
    background-color: black;
    color: white;
    padding-top: 70px;

    ul {
        list-style-type: none;

    }

    h5 {
        font-weight: bolder;
        margin-bottom: 20px;
    }

    address {
        color: grey;
        font-size: 15px;
    }


    a {
        color: grey;

        &:hover {
            color: $red;
        }
    }
}

.icon {
    a {
        margin-right: 15px;

        &:hover {
            filter: invert(50%) sepia(50%) saturate(5) hue-rotate(300deg);
        }
    }

    img {
        filter: invert(100%);
        width: 10px;
    }
}

.footer-bottom {
    height: 60px;
    background-color: black;
    color: grey;

    p {
        padding-top: 15px;
    }
}

.line {
    width: 100%;
    height: 0.5px;
    background-color: #3e3e3e;
}
</style>