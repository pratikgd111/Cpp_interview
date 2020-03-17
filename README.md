# Cpp_interview
post all important questions related to CPP
hacker rank interview kit quotions 
day1
arr[6][6]={INITIALIZE ELEMENTS};
Q1.find the max sum of hourglass in the 6*6 matrix?
Ans->step1:Form 6*6 array and initialise array.
step2:called function sum_Hourglass() from driver function main()
step3:create variable int result=INT_MAX; To store result.
step4:find the last hourglass in the matrix and use there row and column number resp. for limitting the traversing of array using for loop.
step 5:calculate sum of all hourglass (16)
write for(row=0;row<=3;row++)
                 for(col=0;col<=3;col++)
                 int sum+=arr[0][0]+arr[0][1]+arr[0][2]+arr[1][1]+arr[2][0]+arr[2][1]+arr[2][2];
step 6:calculate max sum using built in function 
result=std::max(result,sum);    
step 7:display the result on console.
