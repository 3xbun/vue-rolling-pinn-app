<template>
  <div>
    <Header />
    <div class="container">
      <router-link to="/sales">
        <Btn title="+ New Sales" />
      </router-link>
      <div v-if="onGoing.length > 0">
        <h1>On Going Sales</h1>
        <table v-if="onGoing.length > 0">
          <div v-for="(customer, index) in onGoing" :key="index">
            <tr>
              <td class="name">
                {{ customer.name }}
                <span class="updated">
                  last updated: {{ customer.lastUpdate }}
                </span>
              </td>
              <td class="delete" @click="deleteOngoing(index)">
                <i class="fas fa-minus-circle"></i>
              </td>
            </tr>
            <hr />
          </div>
        </table>
      </div>
    </div>
    <Footer title="Completed Sales" />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";
import Btn from "@/components/Btn.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    Btn,
    Footer
  },
  data() {
    return {
      onGoing: [
        {
          name: "John",
          lastUpdate: "January 10, 09:00"
        },
        {
          name: "Jane",
          lastUpdate: "May 20, 10:20"
        },
        {
          name: "King",
          lastUpdate: "March 5, 22:12"
        },
        {
          name: "Bunn",
          lastUpdate: "Febuary 6, 12:32"
        }
      ]
    };
  },
  methods: {
    deleteOngoing(index) {
      this.onGoing.splice(index, 1);
    }
  }
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background-color: #eaeaea;
}

hr {
  border: 1px solid rgba(105, 75, 100, 0.3);
  margin: 1em auto;
  width: 100%;
}

table {
  margin: auto;
  width: 100%;
  background-color: white;
  margin-top: 1em;
  padding: 1em;
  border-radius: 1em;
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);

  tr {
    display: flex;
    justify-content: space-between;
  }

  td {
    text-align: left;

    .updated {
      font-size: 0.7em;
      color: grey;
    }

    .delete {
      cursor: pointer;
      text-align: right;
    }
  }

  .fa-minus-circle {
    color: grey;
  }
}
</style>
