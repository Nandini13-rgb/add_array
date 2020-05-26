# add_array
Adding one to an array
def add_array(arr):
    if arr == [9] * len(arr):
        arr1 = [1]
        for i in range(len(arr)):
            arr1.append(i * 0)
        return arr1
    else:
        for i in range(len(arr) - 1, -1, -1):
            if arr[i] != 9:
                arr[i] = arr[i] + 1
                break
            if arr[i] == 9:
                arr[i] = 0
                i -= 1

    return arr


# arr = [1,2,3,4]
# arr = [1,2,3,9]
# arr = [1,2,9,9]
arr = [9, 9, 9, 9]
result = add_array(arr)
print(result)
