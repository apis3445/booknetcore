# 9.8 Mejorando tu código

En esta sección voy a explicar como realizar las mejoras de seguridad. Explicare las siguientes:

1. Limitar el número de intentos incorrectos, por ejemplo después de 5 intentos incorrectos mandar un mail con un código que el usuario debe teclear para acceder a su cuenta.
2. Registrar la ciudad (mediante la ip) de donde se conectar normalmente tus usuarios, para que si un usuario se conecta de otra ciudad diferente envies un email notificando el acceso.
3. Puedes agregar un método para revisar si tu token es válido, esto lo puedes realizar con un action filter, o puedes realizarlo con las funciones que proporciona .net, explicaré  la forma con .Net
