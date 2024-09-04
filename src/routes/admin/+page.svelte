<script>
    import { onMount } from 'svelte';
    import { Content as ModalContent, Modal, Trigger as ModalTrigger } from "sv-popup";
	import AddTaskForm from '../../components/+AddTaskForm.svelte';
</script>

<main class="admin-dashboard">
    <h1 class="title">Admin Dashboard</h1><br>

    <Modal button={false}>
        <ModalContent class="modal_content">
            <AddTaskForm />
        </ModalContent>
        <ModalTrigger class="w-[200px] self-center">
            <button class="action ">Add Task</button>
        </ModalTrigger>
    </Modal>
</main>

<style>
    main.admin-dashboard {
        border: 1px solid #ddd;
        display: flex;
        flex-direction: column;
        border-radius: 8px;
    }

   
</style>
