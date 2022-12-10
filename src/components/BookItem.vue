<template>

    <div>

        <h2>Blood Group: {{blood.blood_group}}</h2>
        <h4>Donor: {{blood.donor}}</h4>
        <h4>Recipient: {{blood.recipient}}</h4>
        <h4>Personality: {{blood.personality}}</h4>
    </div>

</template>

<script>


export default{
    name: 'BookItem',
    props:{
        blood: Array
    }
}


</script>

<style scoped>


h4{
    margin: 2px;
}

div{
    background-color: #acf3ef;
    color: black;
    padding: 1em;
}

.red{
background-color: rgb(26, 24, 24) !important;

}
.green{
    color: white;
}


</style>