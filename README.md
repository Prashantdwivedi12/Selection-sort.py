# Selection-sort.py
import random

y = []
for i in range(100):
	y.append(int(round(random.random()*10000)))

def selectSort(lst):
	sorted = 0
	while sorted<len(lst)/2:
		small = sorted
		large = sorted
		for i in range(sorted+1,len(lst)-sorted):
			if lst[i]<lst[small]:
				small = i
			if lst[i]>lst[large]:
				large = i
		lst[sorted], lst[small] = lst[small], lst[sorted]
		lst[len(lst)-1-sorted], lst[large] = lst[large],lst[len(lst)-1-sorted]
		sorted+=1
	print lst

selectSort(x)
