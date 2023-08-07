<template>
  <h1 class="text-center ma-2">Dialogs</h1>

  <v-dialog
    v-model="dialog"
    max-width="600"
    close-delay="300"
    open-on-hover
    no-click-animation="true"
    :scrim="false"
  >
    <template v-slot:activator="{ props }">
      <v-btn v-bind="props" color="warning" class="ma-5"
        >Open Dialog(props)</v-btn
      >
    </template>

    <v-card>
      <v-card-text
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque fugit
        illum corrupti delectus quo voluptas sint odio totam eveniet
        consequatur?</v-card-text
      >
      <v-card-actions>
        <v-btn
          @click="dialog = false"
          color="red"
          max-width="100"
          variant="text"
          >Close</v-btn
        >
      </v-card-actions>
    </v-card>
  </v-dialog>

  <v-btn color="blue" variant="text" @click="dialog1 = true"
    >Open Dialog(v-model)</v-btn
  >

  <v-dialog v-model="dialog1" max-width="700" persistent >
    <v-card>
      <v-card-text
        >Lorem ipsum dolor, sit amet consectetur adipisicing elit. Culpa,
        distinctio!</v-card-text
      >
      <v-btn @click="dialog1 = false" color="red" variant="text">Close</v-btn>
    </v-card>
  </v-dialog>

  <!-- -----------------------------------fullScreen --------------------------------- -->

  <v-btn color="blue" @click="dialog2 = true">FullScreen dialogs</v-btn>
  <v-dialog
    v-model="dialog2"
    fullscreen=""
    transition="dialog-bottom-transition"
  >
    <v-card>
      <v-toolbar dark color="primary">
        <v-btn
          ><v-icon @click="dialog2 = false" icon="mdi-close"></v-icon
        ></v-btn>
        <v-toolbar-title>Message</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn variant="text" prepend-icon="mdi-check">Save</v-btn>
      </v-toolbar>

      <v-list-item title="snehal kanase" subtitle="How are you ?" class="ma-4">
        <template v-slot:prepend><v-icon icon="mdi-account"></v-icon></template>
      </v-list-item>

      <v-divider inset=" "></v-divider>
      <v-list-item title="snehal kanase" subtitle="How are you ?" class="ma-4">
        <template v-slot:prepend><v-icon icon="mdi-account"></v-icon></template>
      </v-list-item>
    </v-card>
  </v-dialog>

  <v-btn @click="dialog3 = true">Overflow</v-btn>
  <v-dialog v-model="dialog3" width="700">
    <v-card>
      <v-card-text
        >Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quas dolor
        iure, hic exercitationem ipsum fugiat at in perferendis provident
        placeat mollitia nihil, minima id nobis omnis est ipsa, expedita unde
        excepturi corporis repudiandae. Vitae itaque sequi culpa provident?
        Ratione iusto facilis veritatis. Perferendis voluptates mollitia earum
        impedit enim nemo omnis optio minus facilis quisquam hic quae officia,
        sit molestiae ratione sapiente ipsum sint officiis repellat odit rerum
        provident! Eligendi qui inventore amet, molestiae accusamus perferendis
        illo, distinctio dicta nam sequi, incidunt porro cum pariatur? Corrupti
        voluptatem blanditiis saepe obcaecati dolorem eius asperiores architecto
        nisi iusto, facere consectetur perspiciatis nulla officiis. Lorem ipsum
        dolor sit amet consectetur adipisicing elit. Eveniet eos soluta beatae
        nulla, illo minus optio labore sit unde quas officiis animi dolor iure
        libero rem quod ab modi vel delectus temporibus deserunt impedit nemo.
        Voluptate cupiditate a recusandae aperiam id exercitationem fugiat
        adipisci deserunt, harum vel fugit fuga accusantium dolores impedit
        dolorum? Rem error esse rerum sed, quia eius pariatur aspernatur fugit
        similique consectetur est ex vero voluptatem quaerat aliquid enim velit
        accusantium neque repellendus eaque deserunt odit, voluptatum nesciunt?
        Facilis eveniet amet cumque corrupti, tempore odio excepturi voluptatem
        ratione dolor cupiditate, temporibus voluptas laudantium quidem nostrum
        cum quae! Porro ipsa sapiente expedita beatae eum delectus fugiat ad
        totam ut consequuntur perspiciatis quos amet dignissimos quod eligendi
        impedit ea consequatur iste distinctio, deserunt molestias. Quam iusto
        ab perferendis mollitia perspiciatis nam distinctio nisi placeat dolorem
        blanditiis eligendi ut magnam, unde quasi deserunt sed omnis itaque
        corporis. Corporis, recusandae minus modi tempora voluptatum quas vitae.
        Expedita laudantium eveniet dolor voluptatibus repudiandae nesciunt
        reprehenderit aperiam suscipit, aliquid dolores est, minus nemo.
        Doloribus id odit commodi saepe expedita, minus delectus voluptatem
        maxime dolor a possimus ex quibusdam numquam quae voluptate similique
        recusandae nemo ratione adipisci perspiciatis. Sunt reprehenderit ipsum
        ut a in.Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quas
        dolor iure, hic exercitationem ipsum fugiat at in perferendis provident
        placeat mollitia nihil, minima id nobis omnis est ipsa, expedita unde
        excepturi corporis repudiandae. Vitae itaque sequi culpa provident?
        Ratione iusto facilis veritatis. Perferendis voluptates mollitia earum
        impedit enim nemo omnis optio minus facilis quisquam hic quae officia,
        sit molestiae ratione sapiente ipsum sint officiis repellat odit rerum
        provident! Eligendi qui inventore amet, molestiae accusamus perferendis
        illo, distinctio dicta nam sequi, incidunt porro cum pariatur? Corrupti
        voluptatem blanditiis saepe obcaecati dolorem eius asperiores architecto
        nisi iusto, facere consectetur perspiciatis nulla officiis. Lorem ipsum
        dolor sit amet consectetur adipisicing elit. Eveniet eos soluta beatae
        nulla, illo minus optio labore sit unde quas officiis animi dolor iure
        libero rem quod ab modi vel delectus temporibus deserunt impedit nemo.
        Voluptate cupiditate a recusandae aperiam id exercitationem fugiat
        adipisci deserunt, harum vel fugit fuga accusantium dolores impedit
        dolorum? Rem error esse rerum sed, quia eius pariatur aspernatur fugit
        similique consectetur est ex vero voluptatem quaerat aliquid enim velit
        accusantium neque repellendus eaque deserunt odit, voluptatum nesciunt?
        Facilis eveniet amet cumque corrupti, tempore odio excepturi voluptatem
        ratione dolor cupiditate, temporibus voluptas laudantium quidem nostrum
        cum quae! Porro ipsa sapiente expedita beatae eum delectus fugiat ad
        totam ut consequuntur perspiciatis quos amet dignissimos quod eligendi
        impedit ea consequatur iste distinctio, deserunt molestias. Quam iusto
        ab perferendis mollitia perspiciatis nam distinctio nisi placeat dolorem
        blanditiis eligendi ut magnam, unde quasi deserunt sed omnis itaque
        corporis. Corporis, recusandae minus modi tempora voluptatum quas vitae.
        Expedita laudantium eveniet dolor voluptatibus repudiandae nesciunt
        reprehenderit aperiam suscipit, aliquid dolores est, minus nemo.
        Doloribus id odit commodi saepe expedita, minus delectus voluptatem
        maxime dolor a possimus ex quibusdam numquam quae voluptate similique
        recusandae nemo ratione adipisci perspiciatis. Sunt reprehenderit ipsum
        ut a in.</v-card-text
      >
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      dialog1: false,
      dialog2: false,
      dialog3: false,
    };
  },
};
</script>