BEGIN tsp_greedy(name_file, distance_file) 

# loading cities
    city_names=read_lines_from(thirty_cities_names.txt)
    distance_matrix=read_2D_floats_from(thirty_cities_dist.txt)
    n=number of cities in city_names
    best_route=EMPTY
    best_distance=INFINITY

# trying each city from starting point
    for start_city from 0 to n-1 do
        visited=empty list
        visited.add(start_city)
        current_city=start_city
        total_distance=0

# building the route
        while number of visited cities<n Do

    # finding next unvisted city
            nearist_city=None
            nearist_distcance=infinite 
            FOR next_city FROM 0 TO n-1 DO
                IF next_city NOT IN visited THEN
                    distance=distance_matrix[current_city][next_city]
                    IF distance<nearest_distance THEN
                        nearest_distance=distance
                        nearest_city=next_city

    # Moves to nearest city
            visited.add(nearest_city)
            total_distance=total_distance + nearest_distance
            current_city=nearest_city
        ENDWHILE loop

# returns to starting city 
        total_distance=total_distance + distance_matrix[current_city][start_city]
        visited.add(start_city)  # completes the loop

# checks for best route 
        IF total_distance<best_distance THEN
            best_distance=total_distance
            best_route=copy_of(visited)
    ENDFOR loop

# prints results
    PRINT "Best greedy route:", convert_indices_to_names(best_route, city_names)
    PRINT "Total distance:", best_distance

END tsp_greedy