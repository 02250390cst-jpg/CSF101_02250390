#Calculate the area of a rectangle given its length and width
x = int(input("Enter the length:"))
y = int(input("Enter the width:"))
area = x * y
print(area)

#Determine if a number is even or odd.
num=int(input("Enter any number to test whether it is odd or even:"))
if(num % 2) == 0:
print("The number is even")
else:
print("The number is odd")

#Convert temperature from Celsius to Fahrenheit.
temp_celcuis = int(input("Enter temperature in celcius:"))
fahrenheit = (1.8 \* temp_celcuis) + 32
print(fahrenheit)