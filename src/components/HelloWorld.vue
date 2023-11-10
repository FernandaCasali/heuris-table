    <template>
  <v-data-table
    :headers="headers"
    :items="pesos"
    class="mx-auto bg-secondary rounded-lg"
    :class="`elevation-${14}`"
    max-width="400"
    hide-default-footer
  >
    <template v-slot:item="{ item }">
      <tr>
        <td>{{ item.name }}</td>
        <td>
          <v-checkbox
            v-model="item.um"
            value
            @change="handleCheckboxChange(item, 'um')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
        <td>
          <v-checkbox
            v-model="item.dois"
            value
            @change="handleCheckboxChange(item, 'dois')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
        <td>
          <v-checkbox
            v-model="item.tres"
            value
            @change="handleCheckboxChange(item, 'tres')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
        <td>
          <v-checkbox
            v-model="item.quatro"
            value
            @change="handleCheckboxChange(item, 'quatro')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
        <td>
          <v-checkbox
            v-model="item.cinco"
            value
            @change="handleCheckboxChange(item, 'cinco')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
        <td>
          <v-checkbox
            v-model="item.seis"
            value
            @change="handleCheckboxChange(item, 'seis')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
        <td>
          <v-checkbox
            v-model="item.sete"
            value
            @change="handleCheckboxChange(item, 'sete')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
        <td>
          <v-checkbox
            v-model="item.oito"
            value
            @change="handleCheckboxChange(item, 'oito')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
        <td>
          <v-checkbox
            v-model="item.nove"
            value
            @change="handleCheckboxChange(item, 'nove')"
            on-icon="mdi-check-circle-outline"
            off-icon="mdi-checkbox-blank-circle-outline"
          ></v-checkbox>
        </td>
      </tr>
    </template>
  </v-data-table>
</template>
    <!-- </v-data-table>
  </div>
</template> -->

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      singleSelect: true,
      selected: [],
      pesos: [
        // {
        //   name: 'H1',
        //   um: false,
        //   dois: false,
        //   tres: false,
        //   quatro: false,
        //   cinco: false,
        //   seis: false,
        //   sete: false,
        //   oito: false,
        //   nove: false,
        // },
        {
          name: "H2",
          um: false,
          dois: false,
          tres: false,
          quatro: false,
          cinco: false,
          seis: false,
          sete: false,
          oito: false,
          nove: false,
        },
        {
          name: "H3",
          um: false,
          dois: false,
          tres: false,
          quatro: false,
          cinco: false,
          seis: false,
          sete: false,
          oito: false,
          nove: false,
        },
        {
          name: "H4",
          um: false,
          dois: false,
          tres: false,
          quatro: false,
          cinco: false,
          seis: false,
          sete: false,
          oito: false,
          nove: false,
        },
        {
          name: "H5",
          um: false,
          dois: false,
          tres: false,
          quatro: false,
          cinco: false,
          seis: false,
          sete: false,
          oito: false,
          nove: false,
        },
      ],
      headers: [
        {
          text: "Heuristicas",
          align: "start",
          sortable: false,
          value: "name",
        },
        { text: "1", value: "um" },
        { text: "2", value: "dois" },
        { text: "3", value: "tres" },
        { text: "4", value: "quatro" },
        { text: "5", value: "cinco" },
        { text: "6", value: "seis" },
        { text: "7", value: "sete" },
        { text: "8", value: "oito" },
        { text: "9", value: "nove" },
      ],
    };
  },
  methods: {
    handleCheckboxChange(row, field) {
      Object.keys(row).forEach((key) => {
        console.log(row[key]);
        if (key !== 'name' && key !== field) {
          row[key] = false;
        }
      });
    },
  },
};
</script>



<style>
</style>