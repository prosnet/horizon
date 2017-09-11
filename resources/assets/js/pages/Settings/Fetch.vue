<script type="text/ecmascript-6">
    import Spinner from '../../components/Loaders/Spinner.vue'
    import Message from '../../components/Messages/Message.vue'

    export default {
        components: {Message, Spinner},


        /**
         * The component's data.
         */
        data() {
            return {
                loadingSettings: true,
                settings: null
            };
        },


        /**
         * Prepare the component.
         */
        mounted() {
            this.loadSettings();
        },


        methods: {
            /**
             * Load settings.
             */
            loadSettings() {
                this.loadingSettings = true;

                this.$http.get('/api/booking/settings?type=1')
                    .then(response => {
                        this.settings = response.data.data;

                        this.loadingSettings = false;
                    });
            },

            /**
             * Save settings.
             */
            saveSettings() {
                this.loadingSettings = true;

                this.$http.post('/api/booking/settings', this.settings)
                    .then(response => {
                        this.loadingSettings = false;
                    });
            }
        }
    }
</script>

<template>
    <div>
        <div v-if="loadingSettings" style="text-align: center; margin: 50px;">
            <spinner/>
        </div>

        <form>
            <div v-if="!loadingSettings" class="df aic acc pa4 settings">
                <div class="ft15">
                    <input type="hidden" name="type" id="type" value="1" class="form-control">

                    <div class="form-group" style="margin-bottom: 20px">
                        <input type="radio" name="active" id="enabled" value="1" v-model="settings.active">
                        <label for="enabled">Enabled</label>
                        <br>
                        <input type="radio" name="active" id="disabled" value="0" v-model="settings.active">
                        <label for="disabled">Disabled</label>
                    </div>

                    <div class="form-group">
                        <label for="interval">Interval (in minutes):</label>
                        <input v-model="settings.interval" type="number" name="interval" id="interval"
                               class="form-control">
                    </div>

                    <div class="btn-group pv2">
                        <button v-on:click="saveSettings" type="button" class="btn btn-primary btn-md">Save</button>
                        <!--<button type="button" class="btn btn-primary btn-md">Restore defaults</button>-->
                    </div>
                </div>
            </div>
        </form>
    </div>
</template>
