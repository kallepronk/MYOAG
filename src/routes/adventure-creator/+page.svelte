<script>
    import TextInput from "./TextInput.svelte";
    import Modal from "../../shared/Modal.svelte";
    const answers = {
        setting: "",
        hero: "",
    }

    let showModal = false;

     function setModalFalse() {
        showModal = false;
    }

    function createAdventure() {
        console.log(answers)
        setModalFalse()
    }

    function handleSubmit() {
        showModal = true
    }
</script>

<!-- Modal opens when all settings have been filled in -->
<Modal {showModal} on:click={setModalFalse}>
    <div slot="title">
        <h2>Confirm your choice:</h2>
    </div>
    <h3 class="font-extrabold">Setting:</h3>
    <p>{answers.setting}</p>
    <h3 class="font-extrabold">Hero:</h3>
    <p>{answers.hero}</p>
    <button class="bg-red-600 p-4 rounded-2xl" on:click={setModalFalse}>Cancel</button>
    <button class="bg-green-600 p-4 rounded-2xl" on:click={createAdventure}>Confirm</button>
</Modal>


<!-- Page -->
<h1 class="text-center font-extrabold text-5xl mb-24 mt-4 block">Create Your Own Adventure Game!</h1>

<form on:submit={handleSubmit}>
    <TextInput bind:input={answers.setting}
            description="Describe the setting of the story (example: A fantasy world full of robots, A cyberpunk city on top of a giant turtle)"/>
    <TextInput bind:input={answers.hero}
            description="Describe your hero. (example: A sky pirate sailing the winds, A software maintainer trapped in the computer)"/>

    <button>Make My Adventure!</button>
</form>


