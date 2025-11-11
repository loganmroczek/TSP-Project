```
helper function to parse txt
    read distance file and parse into lists for each city
    read name file and create list of names
    returns lists

helper function to calculate distance
    for city in the route and back to the first city
        add distances
    return distances

tsp_evolutionary function with the thirty city names and thirty city distances as parameters
    call parse text helper function
    best_route initialized as list 0-29
    call distance helper on best route and save as shortest_distance
    stagnation_count
    stagnation_routes empty list
    stagnation_distances empty list
    
    for generation from 1 to 10000
        if stagnation occurs 3 times
            leave loop
        if no improvement occurs
            append current best_route to stagnation_routes
            append current shortest_distance to stagnation_distance
            make 5 random mutations
            increment stagnation count
    
        save best_route and shortest_distance as parent

        for 1000 offspring:
            make copy of parent as offspring

            switch two random indexes in offspring
            see what the new distance is

            if offspring beats shortest_distance
                change best_route and shortest_route to the offspring values

    find the shortest_distance in the stagnation_distances
    find the accompanying route in the stagnation_routes

    attach route names to the best list
    print results
```