Principles of Financial Computing HW#5
R01944040 �h����

This is a Monte Carlo Simulation program to price a 3-asset single-barrier European knock-out put.

The C++ code is compiled in VS2012�C
�ϥΤF��l��Monte Carlo��k�MBrownian Bridge��i����k�C
��J�O S1, S2, S3, X, H (barrier on S1), t (year), v1 (volatility of 1st asset in %), v2 (volatility of 2nd asset in %), v3 (volatility of 3rd asset in %), rho (the correlations between any two assets in %), r (interest rate in %), n (number of paths), and m (number of time points including today, not needed if the Brownian bridge method is used)�CAnd the terminal payoff is max(X - (S1 + S2 + S3)/3, 0).
�����ܶ��ǿ�J�ƾڨ���o���G�A�䤤�̫�i�H��ܿ�J1�ݨϥ�Brownian Bridge�����G�A�ο�J0���ϥ�Brownian Bridge�C

���Variance Reduction�C
Monte Carlo��k�Φh��path���ƭp��ӹ�{���ġA���ƶV�h�����ȴN�V�����ڻ���C���F��p�~�t�A�o�ӵ{�����ڨϥΤFantithetic variables�A�Q��Var((Y1+Y2)/2)�AY1��Y2�O�P�˪����G(�b�o���@�~���ONormal distribution)�A��Y2���t��Y1�A�o�˴N���C�F1/2��variance�C

���Brownian Bridge���t�״����C
�Q��Brownian Bridge���S�ʥh�w�����|�O�_���IĲ��barrier�C�ڻ{���Q�Φ��覡�ӵ������ȡA�̤j���n�B�O�P�˪�replication��(N)�ɡA���ݭn�b�C�Ӥp���q�������X�@�Ӫѻ��A�]���p��t�׸��֡A�ɶ������׬�O(N)�C�ӭ�l��k��ɶ����Φ��X��������M�ܤ֭n��30���k�Χ�j�~�|����ǽT�A�]��Brownian Bridge����k�i�H�ܤj�������B��t�סC

Testing data:
S1 = 50, S2 = 50, S3 = 50, X = 50, H = 80, t = 1 (year), v1 =30 (%), v2 =30 (%), v3 =30 (%), rho = 40 (%), and r = 6 (%).
���դ����number of time points��m=50�A�o�{���ϥ�Brownian Bridge����k�p��ɶ��|�O�ϥ�Brownian Bridge��50�����k�C��path��n���j�ɥi�H����Pı�XBrownian Bridge��t�ת������C
path��n�V�j�V����, ��n��100�ɡAprice���Ȧb2.9 ~ 3.4���k�A��n��1000�ɡAprice���Ȧb3.0 ~ 3.3���k
Brownian Bridge�����G��n��100�ɤw�g���Ĩ�3.0~3.3���k�A�i���ϥ�Brownian Bridg�վ㪺Monte Carlo Simulation���ֳt�a���Ħܹ�ڻ���C
��n��j�ɨ�ؤ�k���w���Ĩ���p���d��A��p��n��10000�ɡAprice���Ȧb3.14 ~ 3.22���k�A��n��50000�ɡAprice���Ȧb3.16 ~ 3.2���k�C
