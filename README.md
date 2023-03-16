# project-lawnmover-Jonathan-Gaytan-and-Kyle-Dang

Group members:
* Jonathan Gaytan jagaytan@csu.fullerton.edu
* Kyle Dang dangkyle@csu.fullerton.edu

# Alternate Algorithm 

* input -> list of alternated colored disks, int n for amount of runs 
* output -> list of organized disks 

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
<<<<<<< HEAD
  
# Alternate Step Count 

step count = 1 + 1 + 2 + 1 + (n - 0 + 1) * (2 + 2 + max(((n - 0)/2 + 1) * (2 + 1), (((n - 1) - 1)/2 + 1) * (2 + 1)))
step count = 5 + (n + 1) * (4 + max((n/2 + 1) * 3, ((n - 2)/2 + 1) * 3))
step count = 5 + (n + 1) * (4 + max(((n + 2)/2) * 3, ((n - 2 + 2)/2) * 3))
step count = 5 + (n + 1) * (4 + max((3n + 6)/2, (n/2) * 3))
step count = 5 + (n + 1) * (4 + max((3n + 6)/2, 3n/2))
step count = 5 + (n + 1) * (4 + (3n + 6)/2)
step count = 5 + (n + 1) * ((3n + 6 + 8)/2)
step count = 5 + (n + 1) * ((3n + 14)/2)
step count = 5 + ((3n^2 + 14n)/2 + (3n + 14)/2) 
step count = 5 + (3n^2 + 14n + 3n + 14)/2
step count = 5 + (3n^2 + 17n + 14)/2
step count = (3n^2 + 17n + 14 + 10)/2
step count = (3n^2 + 17n + 24)/2
step count = (3n^2 + 17n)/2 + 12  
=======
>>>>>>> 45be35cb3bf086b317bf65b193263e365b46fbba

# Lawnmower Algorithm 

* input -> list of alternate colored disks, int n for runs 
* output -> organized list of disk, int number of swaps 

# Lawnmower Psuedocode  

  //BEFORE APPLICATION
for n at 0 to n / 2
  for position = 0 to rightmost_disk
    
    if disk[position] is out_of_bounds
      break 

    else if disk[position] is white AND position <= 3
      do nothing 
      position+=2 

    else if disk[position] is black AND position > 3 
      do nothing
      position+=2 

    else 
      swap left_disk with right_disk
      position+=2 

  for position = rightmost_disk to 0 

    if disk[position] is black AND position > 3 
      do nothing
      position-=2

    if disk[position] is white AND position <= 3
      do nothing
      position-=2

    else 
      swap right_disk with left_disk 
      position-=2

//AFTER APPLICATION 
for n to n / 2

  for position at 0 to rightmost_disk - 1
  
    if value of left_disk > value of right_disk 
      swap the disks 
      add to numOfSwap
      position++

  for position at rightmost_disk - 2

    if value of left_disk > value of right_disk 
      swap the disks 
      add to numOfSwap
      position--

  return sorted 
