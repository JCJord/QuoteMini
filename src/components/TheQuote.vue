<template>
    <div class="col-sm col-md-4 col-lg-3 blocks">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>

export default {

}
</script>

<style>
.panel-body{
    font-family: 'Dancing Script', cursive;
    font-size:24px;
    color: #6e6e6e; 
    border: 1px solid rgb(182, 179, 179);
    padding: 25px;
    width: 250px;
    margin-right: 100px;
}
.blocks{
    margin-right: 50px;
    margin:20px;
}

.quote{
    cursor:pointer;
    margin-right: 20px;
}

.quote:hover{
    background-color: #ffe2e2;
}
</style>