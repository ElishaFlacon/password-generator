<template>
    <v-container>
        <v-responsive class="mx-auto text-center" max-width="500">

            <v-responsive class="text-h4">
                ГЕНЕРАТОР ПАРОЛЯ v.1.0.0
            </v-responsive>

            <v-col>
                <v-col class="flex" max-width="500">
                    <v-text-field label="Пароль" variant="solo-filled" v-model="password" />
                    <v-select label="Выберете размер пароля" :items="[4, 6, 8, 10, 12, 14, 16, 18, 20]" v-model="size" />
                </v-col>
                <v-btn @click="generation">Сгенерировать пароль</v-btn>
            </v-col>
        </v-responsive>
    </v-container>
</template>


<script>
export default {
    name: 'MainPage',

    data: () => ({
        password: '',
        size: 10,
    }),

    methods: {
        generation() {
            let result = '';
            const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
            const charactersLength = characters.length;

            for (let i = 0; i < this.size; i++) {
                result += characters.charAt(Math.floor(Math.random() * charactersLength));
            }

            this.password = result;
        }
    }


}
</script>