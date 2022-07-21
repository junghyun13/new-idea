# new-idea
# python
# Find the sum of the product of two numbers in all cases of picking two numbers in different positions out of N integers. N개의 정수 중 서로 다른 위치의 두 수를 뽑는 모든 경우의 두 수의 곱의 합을 구하라. 
N=int(input())
a=list(map(int,input().split()))
cnt=sum(a) #리스트안에 있는 숫자를 들을 모두 더한다.
add=0
for aa in a:
    cnt-=aa #cnt가 0이 될때까지 숫자들을 계속 뺀다. 예)리스트안에 2,3이 있다면 5-2,(5-2)-3
    add+=aa*cnt #cnt에서 뺀 숫자와 cnt를 곱한다. 예)2*(5-2)+3*(5-2-3)
print(add)
#result--> 3  2 3 4  26
