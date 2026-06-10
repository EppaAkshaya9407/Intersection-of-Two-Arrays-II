# Intersection-of-Two-Arrays-II
nums1 = list(map(int, input("Enter nums1: ").split()))
nums2 = list(map(int, input("Enter nums2: ").split()))
a = sorted(nums1)
b = sorted(nums2)
n = len(a)
m = len(b)
r = []
res = [0] * m
for i in range(n):
    for j in range(m):
        if not res[j] and a[i] == b[j]:
            r.append(a[i])
            res[j] = 1
            break
print(r)
