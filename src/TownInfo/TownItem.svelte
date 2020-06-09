<script>

    export let name;
    export let numOfSys;
    export let time;
    export let contact;
    export let phoneNum;
    export let address;
    export let notes;


</script>

<style>
    #townCard {
        text-align: center;
    }

</style>


<div id="townCard">
    <section id="townSection">
        <h4>{time}</h4>
        <div>{name}</div>
        <div>Number of systems: {numOfSys}</div>
        <div>{address}</div>
        <div>Contact: {contact}</div>
        <div>Phone: {phoneNum}</div>
        <p>Notes: {notes}</p>
    </section>
    
</div>