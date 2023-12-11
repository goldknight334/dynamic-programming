# dynamic-programming
#include<iostream>
#include<vector>
#include<queue>
#include<set>
using namespace std;



//MAXIMUM SUM OF ADJACENT ELEMENTS

/* int f(int ind, vector<int> &nums ,vector<int> &dp){
    if(ind == 0) return nums[ind];
    if(ind < 0) return 0;
    if(dp[ind] != 1) return dp[ind];
    
    int pick =nums[ind] + f(ind-2,nums,dp);
    int notPick = 0+f(ind - 1,nums,dp);

    return dp[ind] = max(pick,notPick);
}

int maximumAdjacentSum(vector<int> &nums){
    int n = nums.size();
    vector<int> dp(n,-1);
    return f(n-1,nums,dp);
}
*/



//MAXIMUM SUM OF ADJACENT ELEMENTS WITH OPTIMISATION


/*int f(int ind , vector<int> &nums,vector<int> &dp){
    if(ind == 0) return nums[ind];
    if(ind < 0) return 0;
    if(dp[ind] != -1) return dp[ind];

    int pick = nums[ind] + f(ind-2,nums,dp);
    int notPick = 0+f(ind-1,nums,dp);
    return dp[ind] = max(pick,notPick);
}

int maximumAdjacentSum(vector<int> &nums){
    int n = nums.size();
    int prev = nums[0];
    int prev2 = 0;
    for(int i=1;i<n;i++){
        int take = nums[i];
        if(i>1) take+=prev2;

        int notTake=0+prev;

        int curri = max(take,notTake);
        prev2 =prev;
        prev = curri;
    }
    return prev;
}
*/


//HOUSE ROBBER

/*int maximumAdjacentSum(vector<int> &nums){
    int n = nums.size();
    int prev = nums[0];
    int prev2 = 0;
    for(int i=1;i<n;i++){
        int take = nums[i];
        if(i>1) take+=prev2;

        int notTake=0+prev;

        int curri = max(take,notTake);
        prev2 =prev;
        prev = curri;
    }
    return prev;
}


long long int houseRobber(vector<int> &valueInHouse){
    vector<int> temp1,temp2;
    int n = valueInHouse.size();
    if(n == 1) return valueInHouse[0];
    for(int i=0;i<n;i++){
        if(i != 0) temp1.push_back(valueInHouse[i]);
        if(i != n-1) temp2.push_back(valueInHouse[i]);
    }
    return max(maximumAdjacentSum(temp1),maximumAdjacentSum(temp2));
}
*/
