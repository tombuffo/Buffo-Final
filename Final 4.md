# Past Work
<p> Here is some of my past work in this class, it is code to estimate how long and how much it costs to get something painted.</p>

`
import math
print("This program calculates the total cost of a paint job.")

do_calculation = True
while(do_calculation):
    
    while(True):
        try:
            sqft_wallspace = int(input("Enter the square feet of wall space" +
                           " that has to be painted: "))
            if (sqft_wallspace <= 0):
                print("Invalid. The value has to be greater than 0.")
                continue               
        except ValueError:
            print("The value you entered is invalid. Only numerical values are valid.")
        else:
            print("Successfully entered.")
            break

    while(True):
        try:
            paint_price_per_gallon = float(input("Enter the price of the paint per gallon: "))
            if (paint_price_per_gallon < 0):
                print("Invalid. The value has to be greater than 0.")
                continue
        except ValueError:
            print("The value you entered is invalid. Only numerical values are valid.")
        else:
            print("Successfully entered.")
            break



    paint_required = math.ceil(sqft_wallspace / 350)
    paintCost = paint_price_per_gallon * paint_required

    laborReq = (sqft_wallspace / 350) * 6
    laborCharges = laborReq * 62.25


    totalCost = laborCharges + paintCost

    print("Information for the paint job.")
    print("- Number of gallons required: ", + paint_required)
    print("- Hours of labor required: ", format(laborReq, ',.1f'), sep='')
    print("- Cost of paint: $", format(paintCost, ',.2f'), sep='')
    print("- Labor charges: $", format(laborCharges, ',.2f'), sep='')
    print("- Total cost of the paint job: $", format(totalCost, ',.2f'), sep='')
    another_calculation = input("Would you like to do another calculation? (Enter 'y' for Yes, 'n' for No: ")
    if (another_calculation != "y"):
        do_calculation = False 
 `       
     [Main Page](https://github.com/tombuffo/Buffo-Final/blob/master/Final.md)
