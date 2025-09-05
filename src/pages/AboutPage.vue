<template>
  <q-page padding>
    <div class="flex column items-center q-gutter-xl text-white">
      <h5>A job is worth doing togheter</h5>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Cupiditate rem ut fuga velit
        deleniti suscipit similique animi nesciunt doloribus dolorem unde et adipisci, eligendi
        laboriosam asperiores? Ullam recusandae blanditiis hic?
      </p>
      <div class="flex row justify-between full-width">
        <q-item-section class="flex column items-center q-gutter-md">
          <q-avatar size="200px" class="overlapping">
            <img :src="`https://cdn.quasar.dev/img/avatar1.jpg`" />
          </q-avatar>
          <q-item-label>User 1</q-item-label>
          <q-item-label>Engineering</q-item-label>
          <q-icon name="style" size="3em" />
        </q-item-section>
        <q-item-section class="flex column items-center q-gutter-md">
          <q-avatar size="200px" class="overlapping">
            <img :src="`https://cdn.quasar.dev/img/avatar3.jpg`" />
          </q-avatar>
          <q-item-label>User 2</q-item-label>
          <q-item-label>Engineering</q-item-label>
          <q-icon name="style" size="3em" />
        </q-item-section>
      </div>
    </div>
  </q-page>
</template>

<script setup></script>

<style lang="scss" scoped></style>
