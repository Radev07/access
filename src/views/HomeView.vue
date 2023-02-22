<template>
    <div class="home text-gray-900 flex gap-8 flex-col text-center">

        <h1 class="text-4xl">Sejá bem vindo</h1>

        <img class="w-20 my-5 m-auto" alt="Vue logo" src="../assets/logo.png">


        <div class="flex m-auto gap-5 flex-wrap">
            <app-button color=green>
                <template v-slot:icon>
                    <icon-lock-closed />
                </template>

                Entrar
            </app-button>

            <app-button color="blue">

                <template v-slot:icon>
                    <icon-user-plus />
                </template>

                Cadastrar

            </app-button>

        </div>

        <a @click="previous" class="hover:text-gray-600 text-gray-800 text-sm w-full cursor-pointer">
            Veio ao lugar errado?
        </a>

    </div>
</template>

<script>
    import AppButton from "@/components/Generic/AppButton.vue";
    import IconUserPlus from "@/components/Icons/UserPlus.vue";
    import IconLockClosed from "@/components/Icons/LockClosed.vue";

    export default {
        components: {
            AppButton,
            IconUserPlus,
            IconLockClosed,
        },
        
        methods: {
            previous() {
                window.history.back()
            }
        }
    }
</script>
