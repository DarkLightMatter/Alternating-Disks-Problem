# project-lawnmover-Jonathan-Gaytan-and-Kyle-Dang

Group members:
* Jonathan Gaytan jagaytan@csu.fullerton.edu
* Kyle Dang dangkyle@csu.fullerton.edu

# Alternate Psuedocode

//BEFORE APPLICATION 
for n to n + 1
  for position = 0 to rightmost_disk //EVEN 
  
    if disk[2*position] is out_of_bounds
      break 

    else if disk[2*position - 1] is black 
      i+=2
      switch disk[2*position] with disk[2*position-1]

    else 
      i+=2
      do nothing

  for position = 1 to rightmost_disk-1 //ODD 

    if disk[2*position + 1] is out_of_bounds
      break 

    else if disk[2*position - 2] is black 
      i+=2
      switch disk[2*position +1] with disk[2*position -2]

    else 
      i+=2 
      do nothing 

//AFTER APPLICATION 
for n to n + 1

  check if even or odd 

    if even 

      for position at 0 to rightmost_disk

        if value of left_disk > value of right_disk
          swap position of disks
          add to numOfSwap  
          position += 2
    
    else odd
      
      for position at 1 to rightmost disk - 1
        
        if value of left_disk > value of right_disk
          swap position of disks 
          add to numOfSwap
          position += 2  
  
  return sorted
