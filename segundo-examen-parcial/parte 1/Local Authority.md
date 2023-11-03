# Local Authority

## Objetivo
Can you get the flag? Go to this [website](http://saturn.picoctf.net:59126/) and see what you can discover.

## Solución
```js
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

Para llegar aqui primero se inspecciono la pagina principal, despues de ahi se encontro el login.php, y ahi se encontro secure.js, ahi se encontro los datos de acceso