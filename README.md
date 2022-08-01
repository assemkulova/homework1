# homework1
#Data

revenue <- c(14574.49, 7606.46, 8611.41, 9175.41, 8058.65, 8105.44, 11496.28, 9766.09, 10305.32, 14379.96, 10713.97, 15433.50)

expenses <- c(12051.82, 5695.07, 12319.20, 12089.72, 8658.57, 840.20, 3285.73, 5821.12, 6976.93, 16618.61, 10054.37, 3803.96)


#solution

months = format(ISOdatetime(2022,1:12,1,0,0,0),"%B")


#calculate profit

profit <- revenue-expenses

profit 


#calculate tax

tax <- round(0.30*profit, 2)

tax


#calculate profit after tax

profit.after.tax <- profit-tax

profit.after.tax


#calculate profit margin

profit.margin <- round(profit.after.tax/revenue,2)*100

profit.margin


#calculate the mean after tax for 12 months

mean_pat <- mean(profit.after.tax)

mean_pat


#find months which means are higher the mean

good.months <- which(profit.after.tax > mean_pat)

good.months


#find months which means are less than the mean

bad.months <- which(profit.after.tax < mean_pat)

bad.months


#find the best month

best.month <- which(profit.after.tax == max(profit.after.tax))

best.month


#find the worst month

worst.month <- which(profit.after.tax == min(profit.after.tax))

worst.month


#convert all the calculations to units of 1000 dollars

revenue.1000 <- round(revenue/1000,0)

expenses.1000 <- round(expenses/1000,0) 

profit.1000 <- round(profit/1000,0)

profit.after.tax.1000 <- round(profit.after.tax/1000,0)


#results

revenue.1000

expenses.1000

profit.1000

profit.after.tax.1000

profit.margin

good.months

bad.months

best.month

worst.month
