<template lang="pug">
  .curso-main-container.pb-3
    BannerInterno(icono="far fa-question-circle" titulo="Actividad didáctica")
    .container.tarjeta.tarjeta--blanca.p-4.p-md-5
  
      #Actividad                
        <Actividad :cuestionario="cuestionario"/>
  
  </template>

<script>
import Actividad from '@/components/actividad/Actividad.vue'
export default {
  name: 'ActividadDidactica',
  components: {
    Actividad,
  },
  data: () => ({
    cuestionario: {
      tema: 'Desarrollo del Lenguaje',
      titulo: 'Cuestionario',
      introduccion:
        '<b>Objetivo:</b> Evaluar la comprensión sobre el desarrollo del lenguaje y sus factores influyentes.',
      barajarPreguntas: true,
      preguntas: [
        {
          id: 1,
          texto:
            '¿Cuál es uno de los factores que influyen en el desarrollo del lenguaje?',
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Gramaticalidad universal', esCorrecta: false },
            { id: 'b', texto: 'Contexto social', esCorrecta: true },
            { id: 'c', texto: 'Aprendizaje estructural', esCorrecta: false },
            { id: 'd', texto: 'Memoria a corto plazo', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 2,
          texto:
            'Según la teoría de Chomsky, ¿qué concepto describe la habilidad innata de adquirir un idioma?',
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Contexto social', esCorrecta: false },
            { id: 'b', texto: 'Gramática universal', esCorrecta: true },
            { id: 'c', texto: 'Desarrollo cognitivo', esCorrecta: false },
            { id: 'd', texto: 'Interacción social', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 3,
          texto:
            '¿Qué etapa se caracteriza por la etapa de Refinamiento del Lenguaje?',
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'De 2 a 5 años', esCorrecta: false },
            { id: 'b', texto: 'De 5 a 12 años', esCorrecta: true },
            { id: 'c', texto: 'A partir de 12 años', esCorrecta: false },
            { id: 'd', texto: 'De 0 a 12 meses', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 4,
          texto:
            'En la etapa Pre-lingüística, ¿qué edad tienen generalmente los niños?',
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: '0 a 12 meses', esCorrecta: true },
            { id: 'b', texto: '12 a 24 meses', esCorrecta: false },
            { id: 'c', texto: '2 a 5 años', esCorrecta: false },
            { id: 'd', texto: '5 a 12 años', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 5,
          texto:
            '¿Qué aspecto es clave en la relación entre el desarrollo del lenguaje y el desarrollo cognitivo?',
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Interacción social', esCorrecta: true },
            { id: 'b', texto: 'Potencial innato', esCorrecta: false },
            { id: 'c', texto: 'Cambio de contexto', esCorrecta: false },
            { id: 'd', texto: 'Memoria a largo plazo', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
      ],
      mensaje_final_aprobado: '¡Excelente! Ha superado la actividad.',
      mensaje_final_reprobado:
        'Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>
