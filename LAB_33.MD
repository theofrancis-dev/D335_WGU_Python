** 33.1 LAB: Formatted output: No parking sign

	print('  NO PARKING')
	print('2:00 - 6:00 a.m.')

**33.2 LAB: Input: Mad Lib

	first_name = input()
	generic_location = input()
	whole_number = input()
	plural_noun = input()
	print(first_name, 'went to', generic_location, 'to buy', whole_number, 'different types of', plural_noun)

** 33.3.1: LAB: Convert to dollars

	q = int(input())
	d = int(input())
	n = int(input())
	p = int(input())
	dollars = (q*25 + d*10 + n*5 + p) / 100
	print(f'Amount: ${dollars:.2f}')

** 33.4 LAB: Driving costs

	gas_mile = float (input()) #miles x gallon
	gas_cost = float (input()) #dollars x gallon
	one_mile_cost = gas_mile / gas_cost
	cost_20 = 20 / one_mile_cost
	cost_75 = 75 / one_mile_cost
	cost_500 = 500 / one_mile_cost
	print(f'{cost_20:.2f} {cost_75:.2f} {cost_500:.2f}')

** 33.5 LAB: Input and formatted output: Right-facing arrow

	base_char = input()
	head_char = input()

	row1 = '      ' + head_char
	row2 = base_char * 6 + head_char * 2
	row3 = base_char * 6 + head_char * 3
	''' Type your code here. '''

	print(row1)
	print(row2)
	print(row3)
	print(row2)
	print(row1)

** 33.6 LAB: Phone number breakdown

	phone_number = int(input())
	last = phone_number % 10000
	first = (phone_number // 10000) % 1000
	area = phone_number // 10000000
	print (f'({area}) {first}-{last}')

** 33.7 LAB: Smallest number

	list = []
	for i in range(3):
		n = int (input())
		list.append(n)
	print ( min(list) 

** 33.8 LAB: Exact change

	def add_s (int):
		if (int) > 1:
			return 's'
		return ''
		
	def print_amount(  total, coin, deduction ):
		c = total // deduction
		if (c>0):
			print (f'{c} {coin}{add_s(c)}')
		return total % deduction    
			
	amount = int (input())
	if (amount ==0):
		print ('No change')
		exit (0)
	amount = print_amount (amount, 'Dollar',100)
	amount = print_amount (amount,'Quarter',25)
	amount = print_amount (amount,'Dime',10)
	amount = print_amount (amount,'Nickel',5)

	if (amount>1):
	 print (f'{amount} Pennies')
	elif (amount == 1):
	 print (f'{amount} Penny')
 
** 33.9 LAB: Output range with increment of 5

	first = int (input())
	last = int (input())
	if (first > last):
		print ("Second integer can't be less than the first.")
	else:
		for i in range (first, last+1,5):
			print (i,"",end="")
		print()
	
	
** 33.10.1: LAB: Print string in reverse

	while (True):
		u_str = input ()
		if (u_str=='done') or (u_str=='Done') or (u_str=='d'):
			break
		print (u_str[::-1])
	
	
** 33.11 LAB: Fibonacci sequence

	def fibonacci(n):
		nums = [0,1]    
		if (n<0):
		   return -1  
		for i in range(1,n):       
			nums.append (nums[i-1]+nums[i])                    
		return nums[n]

	if __name__ == '__main__':
		start_num = int(input())
		print(f'fibonacci({start_num}) is {fibonacci(start_num)}')
	

** 33.12 LAB: Calculate average
	
	def calc_average(nums):
		return sum(nums)/len(nums)
		
	if __name__ == '__main__':
		nums = [1, 2, 3, 4, 5]
		print(calc_average(nums))   # calc_average() should return 3.0

**33.13 LAB: Warm up: Text analyzer & modifier

	def get_num_of_characters(input_str):
		return len(input_str)
    
	def output_without_whitespace(input_str):
		input_str = input_str.replace('\t','')
		return input_str.replace(" ","")
    

	if __name__ == '__main__':
		u_str = input ("Enter a sentence or phrase:\n")
		print (f'\nYou entered: {u_str}\n')
		print(f'Number of characters: {get_num_of_characters(u_str)}') 
		print(f'String with no whitespace: {output_without_whitespace(u_str)}')
		

** 33.14 LAB: Palindrome

	u_str = input()
	rev = (u_str.lower().replace(' ',''))[::-1]

	if (u_str.lower().replace(' ','') == rev):
		print (f'{u_str} is a palindrome')
	else:
		print(f'{u_str} is not a palindrome')
		

** 33.15 LAB: Parsing dates

	def get_month_as_int(monthString):
		if monthString == 'January':
			month_int = 1
		elif monthString == 'February':
			month_int = 2
		elif monthString == 'March':
			month_int = 3
		elif monthString == 'April':
			month_int = 4
		elif monthString == 'May':
			month_int = 5
		elif monthString == 'June':
			month_int = 6
		elif monthString == 'July':
			month_int = 7
		elif monthString == 'August':
			month_int = 8
		elif monthString == 'September':
			month_int = 9
		elif monthString == 'October':
			month_int = 10
		elif monthString == 'November':
			month_int = 11
		elif monthString == 'December':
			month_int = 12
		else:
			month_int = 0

		return month_int

	while (True):
		user_string = input()
		if (user_string=='-1'):
			break
		tokens = user_string.split(" ")    
		#check numbers of tokens are correct
		if (len(tokens)== 3):        
			month = get_month_as_int(tokens[0])        
			if month > 0:
				day = tokens[1][:-1]            
				if (day.isdigit() and (tokens[1][-1]==',')):
					print (f'{month}/{day}/{tokens[2]}')
					
					
** 33.16 LAB: Car wash

	services = { 'Air freshener' : 1 , 'Rain repellent': 2, 'Tire shine' : 2, 'Wax' : 3, 'Vacuum' : 5 }
	base_wash = 10
	total = 10

	service_choice1 = input()
	service_choice2 = input()
	s1 = services.get(service_choice1)
	s2 = services.get(service_choice2)

	print ('ZyCar Wash')
	print ('Base car wash -- $10')

	if s1:
		total = total + s1
		print (f'{service_choice1} -- ${s1}')

	if s2:
		total = total + s2
		print (f'{service_choice2} -- ${s2}')

	print('----')
	print (f'Total price: ${total}')

** 33.17 LAB: Simple integer division - multiple exception handlers

	try:
		user_num = int (input())
		div_num = int (input())
		print ( user_num // div_num )
	except ZeroDivisionError:
		print('Zero Division Exception: integer division or modulo by zero')
	except ValueError as err:
		print('Input Exception:',err)
		
		
** 33.18 LAB: Step counter - exceptions

	def steps_to_miles( steps ):
		if steps < 0:
			raise ValueError ('Exception: Negative step count entered.')
				
		return steps / 2000

	if __name__ == '__main__':
		try:
			st = int (input())
			miles = steps_to_miles (st)
			print(f'{miles:.2f}')
		except ValueError as err:
			print (err)
			

** 33.19 LAB: Thesaurus

	synonyms = {}   # Define dictionary

	try:
		word = input()
		char = input()
		filename = word + '.txt'
		with open(filename,'r') as file:
			lines = file.readlines()
			
			for line in lines:            
				synonyms[line[0]] = line.strip() # Remove newline character
				
				
		if synonyms.get(char):
			print ('\n'.join (synonyms.get(char).split() ))        
		else:
			print (f'No synonyms for {word} begin with {char}.')
	except Exception as err:
		print ('Exception: ',err)
		
	33.20 LAB: Word frequencies (lists)

	filename = input()
	words = {}
	try:
		with open(filename,'r') as file:
			lines = csv.reader (file, delimiter=',')
		 
			for line in lines:          
				for word in line:                             
					c = words.setdefault(word, 0)                
					words[word]+=1                
		
		for w,c in words.items():
			print (w,c)
			
	except Exception as err:
		print(err)
		
** 33.20 LAB: Word frequencies (lists)

import csv

filename = input()
words = {}
try:
    with open(filename,'r') as file:
        lines = csv.reader (file, delimiter=',')
     
        for line in lines:          
            for word in line:                             
                c = words.setdefault(word, 0)                
                words[word]+=1                
    
    for w,c in words.items():
        print (w,c)
        
except Exception as err:
    print(err)
    
