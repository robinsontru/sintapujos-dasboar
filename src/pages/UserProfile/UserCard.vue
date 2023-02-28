<template>
  <card class="card-user">
    <div slot="image">
      <img src="@/assets/img/logo-sena-verde.png" alt="..." />
    </div>
    <div>
      <div class="author">
        <img
          class="avatar border-white"
          src="@/assets/img/tim_80x80.png"
          alt="..."
        />
        <h4 class="title">
          psicóloga
          <br />
          <a href="#">
            <small>@psicóloga</small>
          </a>
        </h4>
      </div>
      <p class="description text-center">
        “La acción puede no siempre atraer la felicidad, pero no hay felicidad sin acción”
   
       
      </p>
    </div>
    <hr />
    <div class="text-center">
      <div class="row">
        <div
          v-for="(info, index) in details"
          :key="index"
          :class="getClasses(index)"
        >
          <h5>
            {{ info.title }}
            <br />
            <small>{{ info.subTitle }}</small>
          </h5>
        </div>
      </div>
    </div>
  </card>
</template>
<script>
export default {
  data() {
    return {
      details: [
        {
          title: "24",
          subTitle: "edad",
        },
        {
          title: "26546549442",
          subTitle: "targeta profesoinal ",
        },
        {
          title: "popayan",
          subTitle: "ciudad ",
        },
      ],
    };
  },
  methods: {
    getClasses(index) {
      var remainder = index % 3;
      if (remainder === 0) {
        return "col-lg-3 offset-lg-1";
      } else if (remainder === 2) {
        return "col-lg-4";
      } else {
        return "col-lg-3";
      }
    },
  },
};
</script>
<style></style>
