<template lang="pug">
  .curso-main-container.pb-3
    BannerInterno(icono="far fa-question-circle" titulo="Actividad didáctica")
    .container.tarjeta.tarjeta--blanca.p-4.p-md-5
      // Para cuestionario usar: ActividadController(:cuestionario="cuestionario") 
      // Para parrafo usar: ActividadController(:parrafo="parrafo")
      ActividadController(:cuestionario="cuestionario")
  </template>

<script>
import ActividadController from '@ecored-sena/base-kit/plugin/components/actividad/ActividadController.vue'

export default {
  name: 'ActividadDidactica',
  components: {
    ActividadController,
  },
  data: () => ({
    cuestionario: {
      tema: 'Logística comercial',
      titulo: 'Cuestionario: logística comercial.',
      introduccion:
        '<b> Objetivo:</b> verificar la comprensión de los conceptos fundamentales relacionados con la logística comercial, el almacenamiento, el recibo, el despacho, el manejo de datos, el <i>picking</i>, el <i>packing</i>, la carga, las BPM y la seguridad y salud en el trabajo.',
      barajarPreguntas: true,
      titulo_aprobado: '¡BUEN TRABAJO!',
      titulo_reprobado: 'VUELVA A INTENTARLO',
      preguntas: [
        {
          id: 1,
          texto:
            'En las operaciones de <i>retail</i>, el almacenamiento permite principalmente:',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Guardar mercancías sin registro.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Ubicar, mantener y manipular mercancías de forma planificada.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Eliminar el recibo y despacho.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Reemplazar la preparación de pedidos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 2,
          texto: 'Conocer el volumen mínimo de productos en almacén permite:',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Solicitar existencias a tiempo y evitar faltantes.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Guardar productos obsoletos.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Suspender el registro de inventario.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Eliminar costos de almacenamiento.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 3,
          texto: 'El almacenamiento de materias primas corresponde a:',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Artículos ya vendidos.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Productos terminados de alta rotación.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Materiales en estado puro, cercanos a producción.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Refacciones para reparar unidades.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 4,
          texto: 'La zona de almacenamiento debe asegurar:',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Solo espacios administrativos.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Apariencia de las estanterías.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Ausencia de tecnología.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Capacidad de almacenamiento y facilidad para el <i>picking</i>.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 5,
          texto: 'En el recibo, la orden de compra sirve para:',
          imagen: require('@/assets/actividad/imagen05.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Formalizar características, cantidades y condiciones del pedido.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Evitar la verificación de mercancía.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Cerrar la entrega al cliente final.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Omitir protocolos de seguridad.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 6,
          texto: 'Los formatos usados en las operaciones de recibo ayudan a:',
          imagen: require('@/assets/actividad/imagen6.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Evitar el registro de entradas y salidas.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Conocer inventario, costo de venta y utilidad o pérdida.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Eliminar la trazabilidad.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Reemplazar la ficha técnica.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 7,
          texto: 'El despacho en logística es:',
          imagen: require('@/assets/actividad/imagen7.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'El primer almacenamiento.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'La clasificación del envase.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'El último contacto del producto con el almacén antes de entregarlo.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'El análisis de ventas semanales.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 8,
          texto: 'La orden de despacho se integra por:',
          imagen: require('@/assets/actividad/imagen8.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Resumen de mercancía, planilla de entrega y factura de venta.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Ficha nutricional, organigrama y política preventiva.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Acta de capacitación y reporte de riesgos.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Solicitud de crédito e informe audiovisual.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 9,
          texto: 'El manejo responsable de datos permite:',
          imagen: require('@/assets/actividad/imagen9.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Tomar decisiones con información precisa sobre la operación.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Evitar sistemas de control.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Impedir el intercambio de información.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Almacenar datos sin uso operativo.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 10,
          texto: 'El EDI facilita la logística porque:',
          imagen: require('@/assets/actividad/imagen10.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Reemplaza todo documento físico.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Intercambia información comercial estructurada y clara.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Elimina códigos de barras y RFID.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Solo guarda datos no estructurados.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 11,
          texto: 'El <i>picking</i> consiste en:',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Seleccionar y preparar productos solicitados.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Cerrar envases farmacéuticos.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Agrupar cargas en <i>pallets</i>.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Analizar datos masivos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 12,
          texto: 'El envase de un producto cumple la función de:',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Agrupar cargas terciarias.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Definir rutas de transporte.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Contener, proteger, conservar y facilitar la manipulación.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Medir el área del almacén.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 13,
          texto: 'Un tapón de seguridad de un envase se usa para:',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Aumentar la carga vehicular.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Conservar el producto y dificultar aperturas no deseadas.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Convertir embalajes.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Reemplazar la rotulación.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 14,
          texto: 'El empaque adecuado debe:',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Atender solo la apariencia.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Reducir la sujeción.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Evitar embalajes secundarios.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Proteger de golpes y optimizar el espacio.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 15,
          texto: 'El embalaje primario se caracteriza porque:',
          imagen: require('@/assets/actividad/imagen05.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Está en contacto directo con el producto.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Solo consolida cargas.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Agrupa cajas con plástico.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'No incide en la presentación.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 16,
          texto: 'El vehículo de transporte se elige según:',
          imagen: require('@/assets/actividad/imagen6.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Los informes de ventas.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Naturaleza, cantidad, forma, volumen y peso de la mercancía.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'El diseño de etiquetas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'El número de departamentos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 17,
          texto: 'La unitarización busca:',
          imagen: require('@/assets/actividad/imagen7.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Separar productos como carga suelta.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Sustituir la rotulación.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Agrupar mercancías para protegerlas y transportarlas.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Eliminar <i>pallets</i> o contenedores.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 18,
          texto: 'Una rotulación clara permite:',
          imagen: require('@/assets/actividad/imagen8.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Ocultar datos críticos.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Identificar y seguir productos en la cadena logística.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Aumentar el peso permitido.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Reemplazar normas técnicas.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 19,
          texto: 'El cubicaje eficiente consiste en:',
          imagen: require('@/assets/actividad/imagen9.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Acomodar mercancías respetando espacio y límites.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Transportar sin considerar normas.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Separar unidades consolidadas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Clasificar envases por material.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },

        {
          id: 20,
          texto: 'Las BPM y la seguridad y salud en el trabajo buscan:',
          imagen: require('@/assets/actividad/imagen10.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Reemplazar el control de calidad.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Reducir la higiene personal.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Prevenir riesgos y proteger a trabajadores y consumidores.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Limitar la logística al transporte.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
      ],
      mensaje_final_aprobado: 'Ha superado la actividad.',
      mensaje_final_reprobado:
        'No ha superado la actividad. Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>
