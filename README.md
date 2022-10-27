# Python-projects
programming codes for all projects


#This is about Josephus problem: Given the total number of person N and a number k which indicates that k-1 persons are skipped and the kth person is killed in a circle. Find the last person standing in the circle.

def Josephus(N, k):
  lst = list(range(1,N+1))
  kill_person = 0
  while len(lst) > 1:
    kill_person = (k+kill_person-1)%len(lst)
    lst.pop(kill_person)
  return lst[0]
