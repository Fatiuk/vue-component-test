<template>
  <div class="profile-card">
    <div class="profile-wrap">
      <img class="profile-wrap__image" :src="avatar" :alt="username" />
      <p class="profile-wrap__username">{{ username }}</p>
      <p class="profile-wrap__tag">@{{ tag }}</p>
      <p class="profile-wrap__location">{{ location }}</p>
    </div>

    <ul class="profile-card__list">
      <li class="profile-card__item">
        <span class="profile-card__label">Followers</span>
        <span class="profile-card__value">{{ followers }}</span>
      </li>
      <li class="profile-card__item">
        <span class="profile-card__label">Views</span>
        <span class="profile-card__value">{{ views }}</span>
      </li>
      <li class="profile-card__item">
        <span class="profile-card__label">Likes</span>
        <span class="profile-card__value">{{ likes }}</span>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.profile-card {
  width: 280px;
  margin: 0 auto;
  margin-top: 48px;
  padding-top: 32px;
  color: #464748;
  background-color: var(--color-background);
  transition: background-color 0.5s;
  border-radius: 6px;
  box-shadow: var(--color-border) 0px 2px 8px;
}
.profile-wrap {
  text-align: center;
  margin-bottom: 30px;
}

.profile-wrap__image {
  width: 180px;
  display: block;
  margin: 0 auto;
  margin-bottom: 24px;
  border-radius: 50%;
}

.profile-wrap__username {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 16px;
}

.profile-wrap__tag {
  font-size: 18px;
  font-weight: 500;
  margin-bottom: 8px;
  color: #949799;
}

.profile-wrap__location {
  font-size: 16px;
  font-weight: 500;
  color: #949799;
}

.profile-card__list {
  display: flex;
  justify-content: space-between;
  margin: 0;
  padding: 0;
  list-style: none;
}

.profile-card__item {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 60px;
  background-color: var(--color-background-soft);
  border: 0.5px solid #00000035;
  cursor: pointer;
  transition: all 0.3s;
}
.profile-card__item:hover {
  background-color: hsla(160, 100%, 37%, 0.2);
}

.profile-card__item:hover .profile-card__label {
  color: hsla(160, 100%, 37%, 1);
}

.profile-card__item:first-child {
  border-bottom-left-radius: 6px;
}

.profile-card__item:last-child {
  border-bottom-right-radius: 6px;
}

.profile-card__label {
  font-size: 14px;
  font-weight: 500;
  color: #87898b;
}

.profile-card__value {
  font-weight: 500;
}
</style>

<script>
import userData from './user.json'

const { avatar, username, tag, location, followers, views, likes } = userData

export default {
  data() {
    return {
      avatar,
      username,
      tag,
      location,
      followers,
      views,
      likes
    }
  }
}
</script>
