<script setup>
import HandShakeSvg from "../components/icons/HandShakeSvg.vue";
import tableStatusCode from "../utils/enums/tableStatusCode";
</script>

<script>
import api from "../plugins/axios";
export default {
  data() {
    return {
      orders: [],
    };
  },
  async created() {
    const response = await api.get("/orders").then((resp) => {
      return resp.data;
    });
    this.orders = response;
  },
  methods: {
    formatDateValue: (item) => {
      return new Date(item).toLocaleDateString();
    },
    formatMoneyValue: (item) => {
      return Number(item).toLocaleString("pt-br", {
        style: "currency",
        currency: "BRL",
      });
    },
    renderTableStatus: (item) => {
      return tableStatusCode[item];
    },
  },
};
</script>

<template>
  <section className="orders-content">
    <div className="title-subtitle-wrapper">
      <div className="orders-title-container">
        <HandShakeSvg />
        <span>Notas fiscais</span>
      </div>
      <div className="orders-subtitle-container">
        <span>Visualize as notas fiscais que você tem.</span>
      </div>
    </div>
    <div className="table-orders-container">
      <table>
        <thead>
          <tr className="table-header-row">
            <th>nota fiscal</th>
            <th>sacado</th>
            <th>cedente</th>
            <th>emissão</th>
            <th>valor</th>
            <th>status</th>
            <th></th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="item in orders"
            v-bind:key="item.id"
            className="table-data-row"
          >
            <td>{{ item?.nNf }}</td>
            <td>{{ item?.buyer?.name }}</td>
            <td>{{ item?.provider?.name }}</td>
            <td>{{ formatDateValue(item.emissionDate) }}</td>
            <td className="featured-value">
              {{ formatMoneyValue(item.value) }}
            </td>
            <td className="featured-value bold">
              {{ renderTableStatus(item?.orderStatusBuyer) }}
            </td>
            <td className="show-buyer-data-btn">
              <span className="bold">Dados do cedente</span>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</template>

<style scoped>
.orders-content {
  padding-left: 48px;
  padding-top: 40px;
  padding-right: 47px;
}

.title-subtitle-wrapper {
  display: flex;
  flex-direction: column;
  row-gap: 5px;
}

.orders-title-container {
  display: flex;
  align-items: center;
  column-gap: 9px;
}

.orders-subtitle-container {
  font-family: "DM Sans";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #727d94;
}

.orders-title-container > span {
  font-family: "DM Sans";
  color: #021b51;
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 28px;
}

.table-orders-container {
  margin-top: 20px;
}

table {
  width: 100%;
}

tbody {
  display: flex;
  flex-direction: column;
  row-gap: 16px;
}

tr.table-header-row {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
  padding-left: 30px;
  margin-bottom: 19px;
  padding-right: 15px;
}

tr.table-header-row > th {
  font-family: "DM Sans";
  font-style: normal;
  font-weight: 700;
  font-size: 12px;
  line-height: 16px;
  /* identical to box height */

  display: flex;
  align-items: center;
  text-transform: uppercase;

  color: #a1a8b8;
}

tr.table-data-row {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
  align-items: center;
  padding-left: 30px;
  padding-right: 15px;
  background: #ffffff;
  height: 48px;
  border: 1px solid #dfe2eb;
  border-radius: 6px;
}

tbody > tr > td {
  font-family: "DM Sans";
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 18px;
  display: flex;
  align-items: center;

  /* N. Dark / 3 */

  color: #4d5566;
}

.featured-value {
  font-weight: 500;
  color: #00ad8c;
}

.show-buyer-data-btn {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  width: 165px;
  height: 32px;

  /* P. Blue / 2 */

  border: 1px solid #cad3ff;
  border-radius: 24px;
  color: #727d94;
}

.bold {
  font-weight: 700;
}
</style>
