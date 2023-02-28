<template>
  <div class="row">
    <div class="col-12">
      <card :title="table1.title" :subTitle="table1.subTitle">
        <div slot="raw-content" class="table-responsive">
          <paper-table :data="table1.data" :columns="table1.columns">
          </paper-table>
        </div>
      </card>
    </div>

    <!-- <div class="col-12">
      <card class="card-plain">
        <div class="table-full-width table-responsive">
          <paper-table
            type="hover"
            :title="table2.title"
            :sub-title="table2.subTitle"
            :data="table2.data"
            :columns="table2.columns"
          >
          </paper-table>
        </div>
      </card>
    </div> -->
  </div>
</template>
<script>
import { PaperTable } from "@/components";
const tableColumns = ["Id", "Name", "numero", "ficha", "Ciudad"];
const tableData = [
  { id: 1,
    name: "juan",
    numero: "3673865432",
    ficha: "24542242",
    ciudad: "Popayan",  },
  {   id: 2,
    name: "manuel",
    numero: "23986789",
    ficha:"2554854",
    ciudad: "Popayan",
},
  {
    id: 3,
    name: " Rodriguez",
    numero: "345643142",
    ficha: "2455242",
    
    ciudad: "Popayan",
  },
  {
    id: 4,
    name: "pedro",
    numero: "3823445735",
    ficha: "2455242",
    ciudad: "Popayan",
  },
  {
    id: 5,
    name: "jorge",
    numero: "6364352542",
    ficha: "2455242",
    ciudad: "Popayan",
  },
];

export default {
  components: {
    PaperTable,
  },
  data() {
    return {
      table1: {
        title: "Tabla de citas confirmadas ",
        subTitle: "Esta es la tabla de los aprendicez  con cita confirmada ",
        columns: [...tableColumns],
        data: [...tableData],
      },
      table2: {
        title: "Table on Plain Background",
        subTitle: "Here is a subtitle for this table",
        columns: [...tableColumns],
        data: [...tableData],
      },
    };
  },
};
</script>
<style></style>
