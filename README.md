# SpotMcCormick.WarehouseSales
Here is a quick dashboard I made of total transactions per warehouse

To get the today transations per warehouse, I had to use 2 tables. The code consited of this 
####
SELECT  sum(T.transactions) as Total_Transactions, T.store_nbr, S.city, S.state, 
FROM `dulcet-hulling-375416.Grocery.Transactions` as T
 join `dulcet-hulling-375416.Grocery.Stores` as S ON T.store_nbr = S.store_nbr
 where T.store_nbr  between 1 and 60
  group by T.store_nbr, S.city, S.state
 order by Total_Transactions desc
 ####
 
 after querying this I downloaded the query as a CSV then uploaded it to tableau and created this 
