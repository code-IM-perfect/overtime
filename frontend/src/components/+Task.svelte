<style>

.tab-container {

    border: 1px solid #ddd;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    background-color: #fff;
}

.tab-heading {
    display: flex;

    background-color: rgb(76, 255,180);
    color: #fff;
    padding: 16px;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
}
.text-primary {
    --tw-text-opacity: 1;
    color: rgb(76 255 180 / var(--tw-text-opacity)) /* #4cffb4 */;
}
.tab-heading h2 {
  flex: 1;
}

.tab-heading h2 {
    margin: 0;
    font-size: 18px;
}

.tab-details {
    padding: 16px;
    color: #333;
}

.tab-details p {
    margin: 0;
}

    </style>
    <div class="tab-container bg-primary">
        <div class="tab-heading">
            <h2>Task Name</h2>
            <h2>Time</h2>
            <h2>Wage</h2>
        </div>
        <div class="tab-details">
            <p>Task Details.</p>
        </div>
    </div>