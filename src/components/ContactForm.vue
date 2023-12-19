<script setup>
import { ref, onMounted ,computed } from 'vue';

const currentYear = ref(new Date().getFullYear());

const copyrightText = computed(() => ` ${currentYear.value} The Cake Boutique. All rights reserved.`);

onMounted(() => {
  // Update the current year every second (you can adjust the interval)
  setInterval(() => {
    currentYear.value = new Date().getFullYear();
  }, 1000);
});
const Copyright=`<svg fill="#000000" width="15px" height="15px" viewBox="-51.2 -51.2 614.40 614.40" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"><rect x="-51.2" y="-51.2" width="614.40" height="614.40" rx="307.2" fill="#fcfcfc" strokewidth="0"></rect></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path d="M256 8C119.033 8 8 119.033 8 256s111.033 248 248 248 248-111.033 248-248S392.967 8 256 8zm117.134 346.753c-1.592 1.867-39.776 45.731-109.851 45.731-84.692 0-144.484-63.26-144.484-145.567 0-81.303 62.004-143.401 143.762-143.401 66.957 0 101.965 37.315 103.422 38.904a12 12 0 0 1 1.238 14.623l-22.38 34.655c-4.049 6.267-12.774 7.351-18.234 2.295-.233-.214-26.529-23.88-61.88-23.88-46.116 0-73.916 33.575-73.916 76.082 0 39.602 25.514 79.692 74.277 79.692 38.697 0 65.28-28.338 65.544-28.625 5.132-5.565 14.059-5.033 18.508 1.053l24.547 33.572a12.001 12.001 0 0 1-.553 14.866z"></path></g></svg>`
const Tiktok = `<svg fill="#000000" width="40px" height="40px" viewBox="-51.2 -51.2 614.40 614.40" id="icons" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"><rect x="-51.2" y="-51.2" width="614.40" height="614.40" rx="307.2" fill="#fcfcfc" strokewidth="0"></rect></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><path d="M412.19,118.66a109.27,109.27,0,0,1-9.45-5.5,132.87,132.87,0,0,1-24.27-20.62c-18.1-20.71-24.86-41.72-27.35-56.43h.1C349.14,23.9,350,16,350.13,16H267.69V334.78c0,4.28,0,8.51-.18,12.69,0,.52-.05,1-.08,1.56,0,.23,0,.47-.05.71,0,.06,0,.12,0,.18a70,70,0,0,1-35.22,55.56,68.8,68.8,0,0,1-34.11,9c-38.41,0-69.54-31.32-69.54-70s31.13-70,69.54-70a68.9,68.9,0,0,1,21.41,3.39l.1-83.94a153.14,153.14,0,0,0-118,34.52,161.79,161.79,0,0,0-35.3,43.53c-3.48,6-16.61,30.11-18.2,69.24-1,22.21,5.67,45.22,8.85,54.73v.2c2,5.6,9.75,24.71,22.38,40.82A167.53,167.53,0,0,0,115,470.66v-.2l.2.2C155.11,497.78,199.36,496,199.36,496c7.66-.31,33.32,0,62.46-13.81,32.32-15.31,50.72-38.12,50.72-38.12a158.46,158.46,0,0,0,27.64-45.93c7.46-19.61,9.95-43.13,9.95-52.53V176.49c1,.6,14.32,9.41,14.32,9.41s19.19,12.3,49.13,20.31c21.48,5.7,50.42,6.9,50.42,6.9V131.27C453.86,132.37,433.27,129.17,412.19,118.66Z"></path></g></svg>`
const Instagram=`<svg width="40px" height="40px" viewBox="-2 -2 24.00 24.00" xmlns="http://www.w3.org/2000/svg" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"><rect x="-2" y="-2" width="24.00" height="24.00" rx="12" fill="#fcfcfc" strokewidth="0"></rect></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <rect x="0" fill="none" width="20" height="20"></rect> <g> <path d="M12.7 10c0-1.5-1.2-2.7-2.7-2.7S7.3 8.5 7.3 10s1.2 2.7 2.7 2.7c1.5 0 2.7-1.2 2.7-2.7zm1.4 0c0 2.3-1.8 4.1-4.1 4.1S5.9 12.3 5.9 10 7.7 5.9 10 5.9s4.1 1.8 4.1 4.1zm1.1-4.3c0 .6-.4 1-1 1s-1-.4-1-1 .4-1 1-1 1 .5 1 1zM10 3.4c-1.2 0-3.7-.1-4.7.3-.7.3-1.3.9-1.5 1.6-.4 1-.3 3.5-.3 4.7s-.1 3.7.3 4.7c.2.7.8 1.3 1.5 1.5 1 .4 3.6.3 4.7.3s3.7.1 4.7-.3c.7-.3 1.2-.8 1.5-1.5.4-1.1.3-3.6.3-4.7s.1-3.7-.3-4.7c-.2-.7-.8-1.3-1.5-1.5-1-.5-3.5-.4-4.7-.4zm8 6.6v3.3c0 1.2-.4 2.4-1.3 3.4-.9.9-2.1 1.3-3.4 1.3H6.7c-1.2 0-2.4-.4-3.4-1.3-.8-.9-1.3-2.1-1.3-3.4V10 6.7c0-1.3.5-2.5 1.3-3.4C4.3 2.5 5.5 2 6.7 2h6.6c1.2 0 2.4.4 3.4 1.3.8.9 1.3 2.1 1.3 3.4V10z"></path> </g> </g></svg>`
const youtube =`<svg fill="#000000" width="40px" height="40px" viewBox="-25.6 -25.6 307.20 307.20" id="Flat" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"><rect x="-25.6" y="-25.6" width="307.20" height="307.20" rx="153.6" fill="#fcfcfc" strokewidth="0"></rect></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path d="M234.33057,69.79736a23.96369,23.96369,0,0,0-14.50489-16.34619C185.55615,40.28223,130.97949,40.39209,128,40.40771c-2.978-.02392-57.55518-.126-91.8252,13.04346A23.96415,23.96415,0,0,0,21.66992,69.79639C19.083,79.72705,16,97.88574,16,128c0,30.11377,3.083,48.27246,5.66943,58.20264a23.96369,23.96369,0,0,0,14.50489,16.34619c32.80615,12.60693,84.22168,13.04541,91.167,13.04541.6206.00049.69678.00049,1.31738,0,6.95069-.00049,58.36231-.43945,91.16651-13.04541a23.96415,23.96415,0,0,0,14.50488-16.34522C236.917,176.273,240,158.11426,240,128,240,97.88623,236.917,79.72754,234.33057,69.79736Zm-72.11182,61.53076-48,32A3.99967,3.99967,0,0,1,108,160V96a3.99968,3.99968,0,0,1,6.21875-3.32813l48,32a3.99979,3.99979,0,0,1,0,6.65625Z"></path> </g></svg>`
const facebook =`<svg fill="#000000" width="40px" height="40px" viewBox="-2.4 -2.4 28.80 28.80" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"><rect x="-2.4" y="-2.4" width="28.80" height="28.80" rx="14.4" fill="#fcfcfc" strokewidth="0"></rect></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path fill-rule="evenodd" d="M15.1742424,5.3203125 L17,5.3203125 L17,2.140625 C16.6856061,2.09765625 15.6022727,2 14.3409091,2 C11.7083333,2 9.90530303,3.65625 9.90530303,6.69921875 L9.90530303,9.5 L7,9.5 L7,13.0546875 L9.90530303,13.0546875 L9.90530303,22 L13.4659091,22 L13.4659091,13.0546875 L16.2537879,13.0546875 L16.6969697,9.5 L13.4659091,9.5 L13.4659091,7.05078125 C13.4659091,6.0234375 13.7424242,5.3203125 15.1742424,5.3203125 Z"></path> </g></svg>`;
</script>
<template>
    <div class="bg-black w-full h-full">
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-3 gap-3 text-white justify-center justify-items-center">
            <div class="flex flex-col gap-4 w-80      justify-center      mt-20 mb-20 p-10">
                <h3>Newsletter</h3>
                <input class="bg-black text-white focus:outline-none border-b border-white" type="text"
                    placeholder="Email Address">
                <input class="bg-black text-white focus:outline-none border-b border-white" type="text"
                    placeholder="First Name">
                <input class="bg-black text-white focus:outline-none border-b border-white" type="text"
                    placeholder="Last Name">
                <input class="bg-black text-white focus:outline-none border-b border-white" type="text"
                    placeholder="Phone Number">
                <h3>Marketing Permissions</h3>
                <div>
                    <div class="ml-4">
                        <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
                        <label class='ml-2' for="vehicle1">Email</label>
                    </div>
                    <div class="ml-4">
                        <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
                        <label class='ml-2'  for="vehicle2">SMS</label>
                    </div>
                </div>
                <p class="text-[12px]">By signing up you are agreeing to receive the latest
                    news and exclusive offers from our restaurants.</p>
                    <button class="text-black bg-white rounded-[25px] w-40 px-2 py-2 hover:bg-gray-400">Subscribe</button>
            </div>
            <div class="flex text-xl flex-col gap-10 w-80 justify-center   mt-20 mb-20 p-10">
                <a href="">Signature Cakes</a>
                <a href="">Bespoke Cakes</a>
                <a href="">Wedding Cakes</a>
                <a href="">Cakesicles</a>
                <a href="">Chocolates</a>
                <a href="">Master Classes</a>
                
            </div>
            <div class="flex flex-col text-xl gap-10 w-80    mt-20 mb-20 p-10">
                <a href="">Payment And Delivery</a>
                <a href="">Help Center</a>
                <a href="">FAQs</a>
                <a href="">Contact Us</a>
                <div class="flex-row flex gap-6">
                    <a href="" v-html="Tiktok"></a>
                    <a href="" v-html="youtube"></a>
                    <a href="" v-html="facebook"></a>
                    <a href="" v-html="Instagram"></a>
                </div>
                <img class="w-46" src="../assets/image/cards.png" alt="">
            </div>
        </div>
        <div class="flex justify-center items-center pb-[40px]">
            <span class="pr-2" v-html="Copyright"></span>
            <p class="text-white">{{ copyrightText }}</p>
        </div>
    </div>
</template>
