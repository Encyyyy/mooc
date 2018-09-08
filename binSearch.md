#自定义函数，实现二分查找，并返回查找结果
def binary_search(find, list1) :
  start = 0
  end = len(list1)
  while start<= end :
    mid = (start + end) // 2
    if list1[mid] == find :
      return mid
    elif list1[mid] > find :
      end = mid -1
    else :
        
      start = mid + 1
  return -1

list1 = [1,2,3,7,8,9,10,5]
#进行二分查找算法前必须保证要查找的序列时有序的，这里假设是升序列表
list1.sort()

print ("原有序列表为:",list1)
find = int(input("请输入要查找的数："))
if find <= 0 :
    print ("请输入正整数！")
    exit()
else:
    result = binary_search(find, list1)
    if result != -1 :
        print ("要找的元素%d的序号为：%d" %(find,result))
    else :
        print ("未找到！")
  
