class Solution {
public:
static bool comp(vector<int>&p1,vector<int>&p2){
    if(p1[0]==p2[0])
    return p1[1]>p2[1];
    return p1[0]<p2[0];
}
    int maxEnvelopes(vector<vector<int>>& en) {
        int n=en.size();
        sort(en.begin(),en.end(),comp);
        vector<int>dp;
        int maxi=1;
        for(int i=0;i<n;i++){
            int height=en[i][1];
            auto it=lower_bound(dp.begin(),dp.end(),height);
            if(it==dp.end())
            dp.push_back(height);
            else
            *it=height;
        }
        return dp.size();
    }
};