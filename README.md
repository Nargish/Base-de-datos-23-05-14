Base-de-datos-23-05-14
======================

CLase de Consulta de tablas

select *from TB_CLIENTE 

SELECT COD_CLI, RAZ_SOC_CLI, RUC_CLI
FROM TB_CLIENTE

SELECT COD_PRO,PRE_PRO,DES_PRO 
FROM TB_PRODUCTO

SELECT COD_PRO Codigo,
       DES_PRO Descripción,
	     PRE_PRO Precio
from TB_PRODUCTO
order by DES_PRO DESC

select COD_PRO,STK_MIN,PRE_PRO 
from TB_PRODUCTO
order by STK_MIN desc,COD_PRO desc

Select top 8 *from TB_PRODUCTO order by COD_PRO deSC 

Select distinct STK_MIN,COD_PRO,PRE_PRO from TB_PRODUCTO
order by STK_MIN


select day(GETDATE())

select month(getdate())

select year(getdate())

select NUM_FAC as 'Numero de Factura',COD_CLI as 'Codigo CLiente', month(FEC_FAC) AS 'MES DE FACTURA'
from TB_FACTURA
order by 'MES DE FACTURA' ASC

select *from TB_PRODUCTO
WHERE UNI_MED='DOC'

select *from TB_PRODUCTO
WHERE PRE_PRO>30

select *from TB_PRODUCTO
WHERE STK_MIN >100 and STK_MIN <=300

select *from TB_VENDEDOR 
WHERE SUELDO_VEN between 800 and 1500

select *from TB_CLIENTE 
WHERE COD_DIS in('D01','D03','D05' )

select *from TB_CLIENTE
where RUC_CLI is not NULL

// 
select *from TB_PROVEEDOR
where RAZ_SOC_PRV LIKE 'D%'

select *from TB_PROVEEDOR
where DIR_PRV LIKE '%DEL%'
