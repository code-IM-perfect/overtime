<script>
  // Example user data
  let user = {
    name: 'Worker name',
    workerid: '0x1111111254fb6c44bAC0beD2854e76F90643097d',
    experience: '150 hours',
    avatar: 'https://via.placeholder.com/150'
  };

  // Example of function to edit user details (not implemented here)
  function editProfile() {
    console.log('Edit profile functionality goes here');
  }
</script>

<style lang="css">
  .profile-container {
   
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    display: flex; /* Use flexbox to position items side by side */
    align-items: center; /* Center items vertically */
  }

  .avatar {
    width: 150px;
    min-height: 150px;
    border-radius: 50%;
    object-fit: cover;
    margin-right: 25px; /* Space between the avatar and the profile info */
  }

  .profile-info {
    display: flex;
    flex-direction: column; /* Stack profile details vertically */
    font-size: 15px;
    height: 150px;
    padding-top: 10px;
    overflow: scroll;
  }

  .profile-info h2 {
    margin: 0;
    margin-bottom: 10px;
    font-size: 30px;
    font-weight: 500;
  }

  .profile-info p {
    margin-bottom: 3px;
    color: #ffffff; /* Slightly darker text color for readability */
    text-overflow: ellipsis;
    
  }

  .profile-info > p > span {
      font-weight: 500;
  }
  .edit-button {
    margin-top: 20px;
    padding: 10px 15px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }

  .edit-button:hover {
    background-color: #0056b3;
  }
</style>

<div class="profile-container sm:max-w-[800px] sm:flex-row flex-col justify-center">
  <img src={user.avatar} alt="User Avatar" class="avatar" />
  <div class="profile-info mt-5">
    <h2 class="text-center sm:text-left">{user.name}</h2>
    <p> <span>Address: </span>{user.workerid} </p>
   <p> <span>Experience: </span>{user.experience} </p>
    <!-- <button class="edit-button" on:click={editProfile}>Edit Profile</button>  -->
  </div>
</div>
