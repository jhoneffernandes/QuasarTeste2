<template>
  <q-page>
<h2 class="text-amber text-center"> Saiba mais sobre o instituto </h2>
<p class="text-center text-amber">Essa é a página sobre.</p>
 <div class="q-pa-md">
    <div class="q-gutter-md">
      <q-carousel
        v-model="slide"
        transition-prev="scale"
        transition-next="scale"
        swipeable
        animated
        control-color="white"
        navigation
        padding
        arrows
        height="300px"
        class="bg-amber text-white shadow-1 rounded-borders"
      >
        <q-carousel-slide name="style" class="column no-wrap flex-center">
          <q-icon name="style" size="56px" />
          <div class="q-mt-md text-center">
            {{ lorem }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="tv" class="column no-wrap flex-center">
          <q-icon name="live_tv" size="56px" />
          <div class="q-mt-md text-center">
            {{ lorem }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="layers" class="column no-wrap flex-center">
          <q-icon name="layers" size="56px" />
          <div class="q-mt-md text-center">
            {{ lorem }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="map" class="column no-wrap flex-center">
          <q-icon name="terrain" size="56px" />
          <div class="q-mt-md text-center">
            {{ lorem }}
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
  </div>

  <p class="text-center text-amber">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Magnam veniam tempora placeat esse enim libero ad, corrupti sit? Sunt, officia? Voluptates voluptate ut ipsa explicabo, quisquam minus libero expedita fugit?
  Fuga cupiditate iusto, molestias corporis delectus repellendus inventore quaerat voluptates impedit hic officiis in ratione, ducimus error provident quibusdam recusandae cumque deserunt aperiam culpa! Provident repellat harum dicta tempora quas!
  Suscipit, dolore! Sequi voluptate iste, qui soluta odio nulla? Facilis incidunt est provident voluptatibus vel. Ducimus, sapiente tempora autem aspernatur nisi placeat dolor nostrum. Facere quaerat eveniet veritatis voluptatibus nam.
  Assumenda quo, officia expedita neque quia perferendis aut, deserunt, sunt maiores id in. Suscipit delectus eveniet, explicabo porro ut maxime sint natus provident sunt velit inventore et possimus nulla. Dolorum.
  Et, amet. At ut quo consequatur saepe, accusantium facere veritatis dolor beatae optio praesentium sunt nam autem vitae itaque non debitis aspernatur! Cumque eius aliquam nobis deserunt repudiandae magni. Temporibus.
  Voluptatem, a possimus ab quam delectus fuga quae quidem. Alias quasi cum ipsa quis quaerat placeat, eaque vero numquam omnis eveniet quod quae at corporis tenetur! Vero sint in nostrum?
  Praesentium doloremque recusandae dicta non enim eius odio ad eos quae perspiciatis nulla accusantium eaque adipisci dolorum, maxime hic, possimus quidem autem tenetur debitis, placeat id est. Voluptas, dolore veritatis?
  Sapiente debitis expedita accusantium incidunt! Soluta dolores, ipsum earum saepe unde ex et sunt odio eum at hic distinctio, eligendi, suscipit corrupti sint maiores illo consequuntur. Assumenda pariatur esse quisquam.
  Rem, explicabo. Delectus magni deserunt dolor! Accusamus fuga omnis quae, error iure pariatur enim, distinctio ratione, odit vel rem vero est neque quibusdam similique culpa dolore ducimus quidem blanditiis soluta.
  Vero, id odit illum ea dolor blanditiis ipsum mollitia deleniti, repellat voluptate fuga autem enim dolores. Optio iure quos soluta minima fuga amet deserunt error. Exercitationem saepe aperiam amet totam.
  Aspernatur consectetur ab expedita nam et voluptatem corrupti facilis aliquam, porro mollitia! Suscipit quis autem quasi, voluptatum officiis assumenda! Laborum quasi deserunt nulla, quis dolore architecto molestias necessitatibus exercitationem illum.
  Veniam pariatur beatae, asperiores sequi, nam deleniti id laboriosam dicta ipsam quibusdam assumenda repellendus atque fugit ratione rem magnam distinctio dolorem perspiciatis fuga repudiandae nobis. Ducimus dolore quo dicta reiciendis.
  Blanditiis voluptate laudantium illo. Adipisci aperiam culpa repellendus ad temporibus. Aut, sed. Sint culpa sapiente possimus facilis hic eius repudiandae neque veritatis est, doloribus numquam assumenda mollitia labore vitae molestiae?
  Alias magnam doloremque quibusdam, ipsa quae dolor et optio tempora cupiditate incidunt iusto fugiat ea error amet inventore totam corrupti molestias voluptatem eligendi. Consequuntur voluptatum aperiam magnam laboriosam, temporibus consequatur?
  Porro perferendis quam, consequatur accusantium sint sit, expedita ea blanditiis vero vel itaque quis atque iure fugiat. Nostrum ad atque ipsum delectus officia velit nisi exercitationem cumque, veniam harum repellat.
  Minima ea sit totam id commodi aperiam officia, expedita a iste, eius veritatis aspernatur quam libero sequi voluptatibus odio possimus et nulla ad inventore. Voluptatum eius debitis qui numquam facere.
  Voluptate quasi eos ullam recusandae cum aliquid, quaerat vero. Laborum, nesciunt magnam provident odit magni nemo iusto pariatur aliquam nobis incidunt rerum dolorem nam facilis ratione, labore dolor aliquid rem?
  Rerum doloribus asperiores in repellendus optio vero quod ea, repellat aliquid eaque exercitationem quisquam odit illum veniam deserunt sed magni cumque deleniti quo, itaque accusamus quos temporibus nisi recusandae? Repudiandae.
  Ab dignissimos ipsam officia! Est, eligendi? Repellendus, accusamus tenetur, quod ab assumenda reprehenderit inventore eius ipsa similique laudantium odit rerum odio nemo commodi officiis eaque nisi. Veniam quod soluta vero.
  Voluptas, doloremque esse cumque est at molestiae quisquam. Minus, nulla. Asperiores ipsam incidunt quo, totam fugiat assumenda earum? Dignissimos incidunt doloremque quas, quae sint deserunt reiciendis esse dolor soluta eos.</p>

  </q-page>
</template>
<script>
export default {
  name: 'PageSobre',
  data () {
    return {
      slide: 'style',
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
}
</script>
<style>
</style>
