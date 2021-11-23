<template>
    <div class="task_form">
        <form @submit="submit">
            <label for="text">Subject</label>
            <input type="text" v-model="text" class="form-control" id="text" />
            <label for="text">Day</label>
            <input type="text" v-model="day" class="form-control" id="text" />
            <label>
                Set reminder
                <input type="checkbox" v-model="reminder" style="margin-left: 10px;" />
            </label>
            <div class="d-flex justify-content-end">
                <Button btnCls="btn btn-primary" text="Add" />
            </div>
        </form>
    </div>
</template>

<script>
import Button from '../components/Button.vue'
export default {
    name: "TaskForm",
    components: { Button },
    data() {
        return {
            text: null,
            day: null,
            reminder: null
        }
    },
    methods: {
        submit(e) {
            console.log(e);
            e.preventDefault();

            const data = {
                id: Math.floor((Math.random() * 1000) + 1),
                text: this.text,
                day: this.day,
                reminder: this.reminder
            }
            this.$emit('add-task', data)
            this.text = ''
            this.day = ''
            this.reminder = ''
        }
    },
    emits: ['add-task']
};
</script>

<style scoped>
.task_form {
    margin: 10px 0;
}
label {
    display: block;
}
</style>