---
ID: 1529
post_title: >
  Obtener los POID de los productos que
  tiene instalado una cuenta en BRM
author: Marcos
post_date: 2016-09-23 11:37:03
post_excerpt: ""
layout: post
permalink: http://172.20.2.115/?p=1529
published: true
---
select ‘0.0.0.1 ‘ || pp.poid_type || ‘ ‘ || pp.poid_id0 || ‘ 0’ as BRM,
pp.service_obj_type, p.name, pp.status
from account_t a
inner join purchased_product_t pp on pp.account_obj_id0 = a.poid_id0
inner join product_t p on p.poid_id0 = pp.product_obj_id0
where a.account_no = ‘101621177582’
and pp.status = 1
union
select ‘0.0.0.1 ‘ || pd.poid_type || ‘ ‘ || pd.poid_id0 || ‘ 0’,
pd.service_obj_type, d.name, pd.status
from pin.account_t a
inner join purchased_discount_t pd on pd.account_obj_id0 = a.poid_id0
inner join discount_t d on d.poid_id0 = pd.discount_obj_id0
where a.account_no = ‘101621177582’
and pd.status =1