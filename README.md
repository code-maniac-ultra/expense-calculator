# expense-calculator
#Defines the basic costs
def hotel_cost(days): 
    return days * 140

#Valid cities
def plane_ride_cost(city): 
    if city == "Charlotte":
        return 183
    elif city == "Tampa":
        return 220
    elif city == "Pittsburgh":
        return 222
    elif city == "Los Angeles":
        return 475
    else:
        print "Not a valid destination"

#Amount of days
def rental_car_cost(days): 
    #cost = raw_input("Daily Cost: ") #40
    total = 40 * days
    if days >=7:
        total = total - 50
    elif days >=3:
        total = total - 20
    return total
    
#Computes total cost    
def trip_cost(city, days, spending_money):
    sum = rental_car_cost(days)+hotel_cost(days)+plane_ride_cost(city)+spending_money
    return sum

print trip_cost(#Place valid city here, #Place days here, #Place spending money here!)
