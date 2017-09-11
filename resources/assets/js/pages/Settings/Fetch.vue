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

            };
        },


        /**
         * Prepare the component.
         */
        mounted() {
        },


        methods: {

        }
    }
</script>

<template>
    <div>
        <div class="df aic acc pa4 settings">
            <div class="ft15">
                <input type="hidden" name="type" id="type" value="1" class="form-control">

                <div class="form-group">
                    <input type="radio" name="active" id="enabled" value="1">
                    <label for="enabled">Enabled</label>
                    <br>
                    <input type="radio" name="active" id="disabled" value="0">
                    <label for="disabled">Disabled</label>
                </div>

                <div class="form-group" style="margin-bottom: 20px">
                    <label for="interval">Interval (in minutes):</label>
                    <input type="number" name="interval" id="interval" class="form-control">
                </div>

                <div class="btn-group pv2">
                    <button type="button" class="btn btn-primary btn-md">Save</button>
                    <button type="button" class="btn btn-primary btn-md">Restore defaults</button>
                </div>
            </div>
        </div>
    </div>
</template>
