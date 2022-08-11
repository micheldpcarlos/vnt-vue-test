<template>
  <div class="users">
    <div class="header">
      <h1>User List</h1>
      <div class="buttons">
        <button>Order By Id</button>
        <button>Order By Name</button>
        <button>Remove First</button>
      </div>
    </div>
    <div class="list-wrapper">
      <Card v-for="user in users" :key="user.id" :user="user" />
    </div>
  </div>
</template>

<script>
import Card from "@/components/Card.vue";
import UsersData from "../data/users.json";

export default {
  name: "HomeView",
  components: {
    Card,
  },
  data() {
    return {
      users: UsersData,
    };
  },
};
</script>

<style lang="scss">
.users {
  .header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #121212;
    z-index: 2;
    position: sticky;
    top: 0;
    padding: 16px;
    margin-bottom: 16px;

    h1 {
      font-size: 16px;
      font-weight: 800;
      color: #fff;
      margin-bottom: 8px;
    }
  }
  .list-wrapper {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
  }
}
</style>
