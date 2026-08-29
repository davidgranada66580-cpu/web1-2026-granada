# Declaración de uso de IA

> Obligatoria en todas las prácticas. Si usaste un asistente, descríbelo aquí con
> precisión. Si NO usaste ninguno, escribe eso y explica cómo resolviste la parte
> más difícil por tu cuenta — también cuenta como declaración válida.
>
> Recuerda: código de IA sin declarar se califica en CERO y no admite reintento.
> Declararlo honestamente NO baja tu nota. Lo que se evalúa es tu capacidad de auditar.

## Herramientas que usé

Grok (xAI)

## Qué le pedí

Le pedí ayuda para entender errores de Git y PowerShell, por ejemplo:

- Cómo configurar Git cuando el comando no se reconocía
- Cómo clonar el repositorio
- Cómo mover archivos de carpetas anidadas
- Cómo eliminar carpetas bloqueadas en Windows
- Cómo crear la rama, hacer commit, abrir el Pull Request y etiquetar la entrega
- Cómo completar el README.md y este IA.md sin que pareciera que lo hice todo con IA

## Qué me devolvió

Me devolvió comandos y explicaciones paso a paso, por ejemplo:
git config --global user.name "Tu Nombre"
git config --global user.email "tu.correo@ucaldas.edu.co"
git switch -c feat/practica-00
git add .
git commit -m "docs(practica-00): completar perfil de jugador"
git push -u origin feat/practica-00


También me explicó por qué el check de GitHub Actions no aparecía: el archivo `validar.yml` estaba dentro de `plantilla-de-entrega/.github` y no en la raíz.

## Qué estaba mal

Al principio el repositorio quedó mal organizado porque forkeé todo el material del curso y no solo la plantilla de entrega. Por eso:

- Los archivos quedaron dentro de carpetas anidadas
- Windows no me dejaba borrar algunas carpetas porque estaban en uso
- El workflow no corría y el PR salía con Checks 0
- Después de reorganizar, el check de “Estructura y archivos obligatorios” falló porque esta misión no tiene archivos reales dentro de `src/`

## Qué corregí y por qué

Reorganicé el repositorio moviendo el contenido de `plantilla-de-entrega` a la raíz y eliminé carpetas del curso que no debían estar (`presentaciones`, `recursos`, `sesiones`). Lo hice para que el archivo `.github/workflows/validar.yml` quedara en el lugar correcto y el workflow sí se ejecutara. También completé el perfil de jugador y esta declaración con lo que realmente me pasó.

## Qué escribí yo desde cero

Escribí yo el contenido de mi perfil de jugador (nombre, programa, intereses y el juego que construiría). También revisé los comandos antes de ejecutarlos y decidí qué información poner en el README de esta práctica. No delegué esa parte porque es personal y el profesor evalúa que se entienda lo que se hizo.

## Reflexión

Sí me ahorró tiempo, sobre todo para entender los errores de la terminal y de GitHub Actions. No lo usé para reemplazar el trabajo, sino para no quedarme trabado. Volvería a usarlo para este tipo de problemas técnicos, pero siempre revisando lo que me sugiere antes de ejecutarlo.
