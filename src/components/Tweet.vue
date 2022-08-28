<template>
  <div className="tweet">
    <ProfileImage image="image" />

    <div className="body">
      <div className="top">
        <User :user="user" />
        <Timestamp :timestamp="timestamp" />
      </div>

      <Message :message="message" />
      <Actions />
    </div>
  </div>
</template>

<script>
import Message from "./Message.vue";
import Actions from "./Actions.vue";
import Timestamp from "./Timestamp.vue";
import User from "./User.vue";
import ProfileImage from "./ProfileImage.vue";

export default {
    props: {
        user: {
            name: String,
            handle: String,
            image: String,
        },
        timestamp: String,
        message: String,
    },
    components: { Message, Actions, Timestamp, User, ProfileImage }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
