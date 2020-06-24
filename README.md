def gen_arm():
	for num in range(1024000, 702648265):
		order = len(str(num))
		sum = 0
		temp = num
		while temp > 1024000:
			digit = temp % 10
			if order == 1:
				order = 0
			sum += digit ** order	
			temp //= 10
		if num == sum:
			yield num
   # order of number
   


values = gen_arm()
for i in values:
	print(i)

o/p - 4782969
