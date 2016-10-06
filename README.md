# 5. Buscar los issues en github

Ahora que estamos seguros que tendremos un repo, podemos usar el API de github
para buscar todos los issues de ese repo. En vez de usar el API directamente,
se puede utilizar el módulo
[node-github](https://github.com/mikedeboer/node-github).

Existe una función
[issues.getForRepo](http://mikedeboer.github.io/node-github/#api-issues-getForRepo)
que busca las issues (recibe un user y un repo). Si no le pasas un callback, te
dará una promesa. La respuesta sera un array de objetos.

En vez de escribir el valor de `repo` a la pantalla, pásaselo a node-github para
buscar los issues de ese repositorio. Tendras que separar `repo` en dos partes
(user y repo), lo cual puedes hacer usando la función `split()` de un string.

Luego usa la función `map` de un array para sacar solo el título de cada issue
(la propiedad se llama `title`).

Finalmente, escribe todos los títulos a la pantalla. En Unix, varios resultados
deben estar separados por el carácter de nueva línea (\n). Puedes o usar otro
`map` con `console.log`, o puedes usar la función `join()` de un array.
