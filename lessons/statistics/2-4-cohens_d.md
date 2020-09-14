def Cohens_D(grp_1, grp_2):

​    grp_1_mean = grp_1.mean()
​    grp_2_mean = grp_2.mean()
​    mean_diff = grp_1_mean - grp_2_mean


    grp_1_var = grp_1.var()
    grp_2_var = grp_2.var()
    
    n_grp_1 = len(grp_1)
    n_grp_2 = len(grp_2)
    
    pool_var = ((n_grp_1*grp_1_var)+(n_grp_2*grp_1_var))/(n_grp_1 + n_grp_1)
    
    pool_std_dev = math.sqrt(pool_var)
    
    Cohens_D_effect = mean_diff/pool_std_dev
    
    return Cohens_D_effect

Cohens_D(firsts.totalwgt_lb, others.totalwgt_lb)

Cohen's D = -0.08626504524149728

The standardized diffrence in total birth weights of the two groups is less than the standardized difference in pregnancy lengths of of the same groups.
