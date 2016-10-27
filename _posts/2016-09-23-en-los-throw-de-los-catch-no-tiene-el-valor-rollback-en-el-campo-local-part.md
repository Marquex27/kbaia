---
ID: 1516
post_title: >
  En los Throw de los Catch no tiene el
  valor “rollback” en el campo
  “Local Part”
author: adminAIA
post_date: 2016-09-23 11:04:05
post_excerpt: ""
layout: post
permalink: http://172.20.2.115/?p=1516
published: true
servicio_aia:
  - ProcessBRMSharingGroupEBF
---
<strong>Descripción:</strong>

Los procesos en BRM no realizan rollback en caso de un error

<strong>Solución:</strong>

se coloca el valor “rollback” en el campo “Local Part” de todos los catch

&nbsp;