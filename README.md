# codeup1
그리디 알고리즘1_3321번

n = int(input())
a, b = map(int, input()) #도우의 가격 토핑의 가격
c = int(input()) #도우의 cal

cal_list = []
for _ in range(n):
    d = int(input()) # 토핑의 cal
    cal_list.append(d)
    
cal_list.sort(reverse=True)

cal_last_list = []

pizza_cal = c
pizza_price = a
pizza_price_cal = c/a
cal_last_list.append(pizza_price_cal)

for i in cal_list:
    pizza_cal = pizza_cal + i #모든 피자의 cal
    pizza_price = pizza_price + b
    pizza_cal_level = pizza_cal/pizza_price
    cal_last_list.append(pizza_cal_level)
k = min(cal_last_list)
print(k)
