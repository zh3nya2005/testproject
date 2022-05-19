<template>
    <div class="container">
        <div class="comments">
            <div class="comments-main">
                <div class="comments-nameuser mb-2"> 
                    <span>Name: {{coms.name}}</span>
                </div>
                <div class="comments-email mb-2">
                    <span>Email: {{coms.email}}</span>
                </div>
                <div class="comments-body">
                    <span>Body: {{coms.body}}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Comments',

    props: [ `coms` ]
}
</script>

<style>
    .background__png{
        background: rgb(197, 182, 182);
        height: 600px;
        border-radius: 20px;
    }

    .png img{
        width: 800px;
        margin: 30px 0 150px 150px;
        border-radius: 20px;
    }
</style>