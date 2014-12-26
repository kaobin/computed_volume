computed_volume
===============

# These codes can help to calculate the volume of surface surround  with a  given function having x,y,z coordinate 
# MATLAB code
f=fit([X,Y],Z,'linearinterp'); %利用线性插值根据散点图模拟出振动曲面的函数
figure(1);
plot(f,'style','Surface');% 画出基于散点图的模拟图
 q= quad2d(f,-0.052,0.047,-0.032,0.019,'AbsTol',0.001) %计算体积，这里的f后面的4个值是
                                                        %X，Y的取值范围，基于以上模拟画出的图像
save mydata;    %保存 workspace到当前文件夹
clear;
