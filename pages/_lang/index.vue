<template>
  <main>
    <app-title :landing="true">
      Aprende mucho en poco tiempo
    </app-title>

    <call-to-action />

    <preview-pills title="Y además...">
      <preview-pills-item v-for="pill in newPills" :key="pill.id" :pill="pill" />
    </preview-pills>

    <preview-pills title="Próximamente...">
      <preview-pills-item v-for="pill in soonPills" :key="pill.id" :pill="pill" />
    </preview-pills>

    <preview-pills title="Cursos completos">
      
    </preview-pills>
  </main>
</template>

<script>
import AppTitle from '~/components/AppTitle';
import PreviewPills from '~/components/PreviewPills';
import PreviewPillsItem from '~/components/PreviewPillsItem';
import CallToAction from '~/components/CallToAction';

export default {
  components: {
    AppTitle,
    PreviewPills,
    PreviewPillsItem,
    CallToAction
  },
  head() {
    return {
      title: 'Home'
    }
  },
  data() {
    return {
      newPills: [
        { id: 1, title: 'Creando un nuevo componente', time: '2 minutos', tags: ['js', 'vue'] },
        { id: 2, title: 'Usando eventos personalizados', time: '4 minutos', tags: ['js', 'vue'] },
        { id: 3, title: '¿Qué es la currificación?', time: '1 minuto', tags: ['funcional'] },
        { id: 4, title: 'Usando las nuevas funcionalidades de vue-cli', time: '5 minutos', tags: ['js', 'vue'] },
        { id: 5, title: 'Tres formas de usar dependencias en Node', time: '5 minutos', tags: ['js', 'node'] }
      ],
      soonPills: [
        { id: 1, title: 'Creando un nuevo componente', time: '2 minutos', tags: ['js', 'vue'] },
        { id: 2, title: 'Usando eventos personalizados', time: '4 minutos', tags: ['js', 'vue'] }
      ]

    }
  }
}
</script>

