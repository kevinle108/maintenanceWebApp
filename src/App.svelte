<script>
    import Header from "./UI/Header.svelte";
    import NavBar from "./NavBar.svelte";
    import TownItem from "./TownInfo/TownItem.svelte";
    //import AddTown from "./AddTown.svelte";


    let name = "";
    let numOfSys = "";
    let time = "";
    let contact = "";
    let phoneNum = "";
    let address = "";
    let notes = "";

    let townList = [
        {
            //id: Math.random(),
            name: 'Hartford',
            numOfSys: 30,
            time: '9:00AM-10:30AM',
            contact: 'Jane Doe',
            phone: '(000) 000-0000',
            address: '555 Street Name City, ST 55555',
            notes: '...big city...'
        },
        {
            id: Math.random(),
            name: 'New Haven',
            numOfSys: 25,
            time: '11:00AM-11:30AM',
            contact: 'John Doe',
            phone: '(999) 123-4567',
            address: '555 Street Name City, ST 66666',
            notes: '...Parking update: park on State St...'
        }
        ];

    function addTownEntry() {
        const newTown = {
            id: Math.random(),
            name: name,
            numOfSys: parseInt(numOfSys),
            time: time,
            contact: contact,
            phone: phoneNum,
            address: address,
            notes: notes
        }

        townList = [newTown, ...townList]
    }

</script>

<style>
    #pageHeader {
        text-align:  center;
    }

    form {
        color:  blue;
        width: 10rem;
        max-width: 90%;
        margin: auto;
    }
</style>


<h1 id="pageHeader">IVS Maintanence App</h1>
<form on:submit|preventDefault={addTownEntry}>
    <div>
        <label for="townName">Town name</label>
        <input type="text" id="townName" bind:value={name}/>
    </div>

    <div>
        <label for="numOfSys">Number of Systems</label>
        <input type="text" id="numOfSys" bind:value={numOfSys}/>
    </div>

    <div>
        <label for="time">Time</label>
        <input type="text" id="time" bind:value={time}/>
    </div>

    <div>
        <label for="contact">Contact</label>
        <input type="text" id="contact" bind:value={contact}/>
    </div>

    <div>
        <label for="phone">Phone</label>
        <input type="text" id="phone" bind:value={phoneNum}/>
    </div>

    <div>
        <label for="address">Address</label>
        <input type="text" id="address" bind:value={address}/>
    </div>

    <div>
        <label for="notes">Notes</label>
        <textarea row="3" id="notes" bind:value={notes}/>
    </div>
    <button type="submit">Save</button>
</form>


{#each townList as town (town.id)}
    <TownItem 
    name={town.name} 
    numOfSys={town.numOfSys} 
    time={town.time} 
    contact={town.contact} 
    phoneNum={town.phone} 
    address={town.address} 
    notes={town.notes}/>
{/each} 
<NavBar/>
