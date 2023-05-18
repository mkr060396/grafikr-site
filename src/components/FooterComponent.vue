<template>
    <div>
        <v-footer color="black" class="pb-5" >
            <v-row class="container-width pt-10">
                <v-col class="text-start" cols="6" lg="3">
                    <h4 class="mb-5 footer-title">Support</h4>
                    <ul>
                        <div class="mb-5">
                            <li>
                                Grafikr A/S
                            </li>
                            <li>
                                CVR: 37783277
                            </li>
                        </div>

                        <div class="mb-5">
                            <li>
                                +45 69 69 29 15
                            </li>
                            <li>
                                kontakt@grafikr.dk
                            </li>
                        </div>

                        <div>
                            <li>
                                Randers:
                                <br>
                                Jernbanegade 12a
                                <br>
                                8900 Randers C
                            </li>
                        </div>
                    </ul>

                </v-col>
                <v-col class="text-start" cols="6" lg="3">
                    <h4 class="mb-5 footer-title">Information</h4>
                    <ul>
                        <li><a href="#">Karriere(4 åbne stillinger)</a></li>
                        <li><a href="#">Hent e-bog om Shopify Plus</a></li>
                        <li><a href="#">Cases</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Om os</a></li>
                        <li><a href="#">Kontakt os</a></li>
                    </ul>

                </v-col>
                <v-col class="text-start" cols="6" lg="3">
                    <h4 class="mb-5 footer-title">Udvalgte cases</h4>
                    <ul>
                        <li><a href="#">ARKK Copenhagen</a></li>
                        <li><a href="#">Basic Apparel</a></li>
                        <li><a href="#">Barons</a></li>
                        <li><a href="#">Camille Brinch Jewellery</a></li>
                        <li><a href="#">EYDA</a></li>
                        <li><a href="#">Noella Fashion</a></li>
                        <li><a href="#">SACKit</a></li>
                    </ul>

                </v-col>
                <v-col cols="6" lg="3">
                    <form class="d-flex flex-column">
                        <input class="mb-3 input-field" type="text" id="name" name="name" placeholder="Navn">
                        <input class="mb-6 input-field" type="email" id="email" name="email" placeholder="E-mail">
                        <button type="button" class="submit-btn d-flex justify-center align-center">Tilmeld vores nyhedsbrev
                            <img class="ml-3" :src="require('@/assets/icons/arrow.png')"> </button>
                    </form>

                </v-col>

                <v-col cols="6" lg="9" class="text-start d-flex align-end">
                    <span class="copyright mb-10">© Grafikr A/S. Alle rettigheder forbeholdt 2023</span>
                </v-col>
                <v-col cols="6" lg="3" class="pa-0">
                    <v-img width="400" :src="require('@/assets/icons/Vector.svg')"></v-img>
                </v-col>
            </v-row>
        </v-footer>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.footer-title {
    font-size: 20px;
}
.input-field {
    background-color: white !important;
    padding: 10px;
    width: 100%;
}

.submit-btn {
    border: 1px solid #FFFFFF;
    background-color: #000000;
    border-radius: 0px;
    padding: 10px;
    width: 100%;
    font-size: 14px;
    text-transform: initial;
}

ul {
    list-style-type: none;
}

li {
    font-size: 14px;
}

a {
    color: #ffff;
    text-decoration: none;
}

.copyright {
    font-size: 14px;
}

@media only screen and (max-width: 600px) {
    li {
        font-size: 12px;
    }

    .input-field {
        background-color: white !important;
        padding: 8px;
        width: 155px;
        font-size: 12px;
    }

    .submit-btn {
        border: 1px solid #FFFFFF;
        background-color: #000000;
        border-radius: 0px;
        padding: 5px;
        width: 155px;
        font-size: 12px;
    }

}
</style>