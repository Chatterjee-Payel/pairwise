# pairwise
bool pairWiseConsecutive(stack<int> s)
{
    //Code here
    vector<int>ans;
    int len=s.size();
    while(!s.empty())
    {
        ans.push_back(s.top());
        s.pop();
    }
    for(int i=0;i<len-1;i++){
        if(abs(ans[i]-ans[i+1])!=1)
        {
            return false;
        }
    }
    return true;
}
