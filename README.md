#Вычисление количества продаж и среднего чека в интервале
#До 1000 р включительно
#От 1000р до 3000р включительно
#От 3000р до 5000р включительно
#Выше 5000 р

sales = [2015, 300.50, 1550, 703, 110, 2146, 733, 114, 161, 310,3155, 853, 114, 131]
#sales = [300, 1000, 3000]

def process_sales(sales):
    # Суммы
    sum1 = 0
    sum2 = 0
    sum3 = 0
    sum4 = 0
    #Количества
    cnt1 = 0
    cnt2 = 0
    cnt3 = 0
    cnt4 = 0
    #Средние
    avg1 = 0
    avg2 = 0
    avg3 = 0
    avg4 = 0
    for sale in sales:
        print(sale, end=' ')
        
        if sale <= 1000:
            sum1 += sale
            cnt1 += 1
        elif sale<= 3000:
            sum2 += sale
            cnt2 += 1
        elif sale<= 5000:
            sum3 += sale
            cnt3 += 1
            
        else:
            sum4 += sale
            cnt4 += 1
            
    # print(" ")
                         
    if cnt1 > 0 : # Иначе оставлем  avg1 равнымм 0
        avg1 = sum1 / cnt1
    if cnt2 > 0 : # Иначе оставлем  avg1 равнымм 0
        avg2 = sum2 / cnt2
    if cnt3 > 0 : # Иначе оставлем  avg1 равнымм 0
        avg3 = sum3 / cnt3
    if cnt4 > 0 : # Иначе оставлем  avg1 равнымм 0
        avg4 = sum4 / cnt4
    
    print("До 1000р включительно:             Количество продаж = " + str(cnt1) + " Средний чек = " + "{:.2f}" . format(avg1) +" p" )
    print("От 1000р до3000 р:  включительно:  Количество продаж = " + str(cnt2) + " Средний чек = " + "{:.2f}" . format(avg2) +" p" )
    print("От 3000р до 5000р:  включительно:  Количество продаж = " + str(cnt3) + " Средний чек = " + "{:.2f}" . format(avg3) +" p" )
    print("От 5000р                           Количество продаж = " + str(cnt4) + " Средний чек = " + "{:.2f}" . format(avg4) +" p" )
    print("Готово!")
    
process_sales(sales)



    


# MyBasicPython
