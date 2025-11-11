```
helper function to parse txt
    read distance file and parse into lists for each city
    read name file and create list of names
    returns lists

helper function to calculate distance
    for city in the route and back to the first city
        add distances
    return distances

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

create list variable for possible routes
tsp_backtracking function with name.txt and distance.txt as parameters
    make list variable global

    call parse txt helper
    make list form 0-6 for the 7 cities

    for second city in len of list of cities
        for the last city from the second city to len of list of cities
            one possible route is equal [0,second_city, last city]  
            make a copy of the city list and remove these 3 to get the remaining cities

            call tsp_recursive with the partial route and remaing
    
    for each route in list of routes
        make a route distances list by calling the distance helper
    
    find the shortest distance from route distances
    find the best_route that matches that distance

    attach route names to best route
    print results
```
