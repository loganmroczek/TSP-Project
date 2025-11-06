```
helper function to parse txt
    read distance file and parse into lists for each city
    read name file and create list of names
    returns lists

helper function tsp_recursive with parameter partial_route, remaining cities
    global routes
    if list of cities is empty
        return partial
    else 
        for city in remaining_cities
            partial copy
            append remaining city

            remaining_cities copy
            remove remaining city
            tsp_recursive(partial copy, remaining copy)
        return routes

create list variable for possible routes
call tsp_backtrack with name.txt and distance.txt as parameters
    make list variable global

    call parse txt helper

    for second city in len of list of cities
        for the last city from the second city to len of list of cities
            one possible route is equal [0,second_city+1, last city]  
            append the one route to the list of routes
    
    call tsp_recursive

```
