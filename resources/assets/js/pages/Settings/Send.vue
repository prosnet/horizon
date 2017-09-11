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
                <div class="form-group">
                    <label for="usr">test:</label>
                    <input type="text" class="form-control" id="usr">
                </div>
                <div class="form-group">
                    <label for="pwd">test:</label>
                    <input type="password" class="form-control" id="pwd">
                </div>

                <div class="btn-group pv2">
                    <button type="button" class="btn btn-primary btn-md">Save</button>
                    <button type="button" class="btn btn-primary btn-md">Restore defaults</button>
                </div>
            </div>
        </div>
    </div>
</template>
