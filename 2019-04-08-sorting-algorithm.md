
'''python
n = int(input().strip())
a = list(map(int, input().strip().split(' ')))
swapped = True
swaps = 0
while swapped:
    swapped = False
    for idx, val in enumerate(a[:-1]):
        if val > a[idx+1]:
            a[idx], a[idx+1] = a[idx+1], a[idx]
            swapped = True
            swaps += 1
print("Array is sorted in {} swaps.".format(swaps))
print("First Element: {}".format(a[0]))
print("Last Element: {}".format(a[-1]))
'''
