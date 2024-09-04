<script>
    import { page } from "$app/stores";
</script>

<h1 class="error-code">{$page.status}</h1>
<h1 class="error-message"> {$page.error?.message}</h1>

<style>
    .error-code{
        font-size: 100px;
        text-align: center;
        font-weight: 600;
        color: #50fcb4;
    }
    .error-message{
        font-size: 30px;
        text-align: center;
        color: #50fcb4;
    }
</style>