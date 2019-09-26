#The Flow of The Installation of Executable Files of "weibo", "apaweibo" And "mo-weibo" of wllv on One's Account on EDA Server of FDU
#Edited by cqli18@fudan.edu.cn
#2019/9/26

Proceed as follows:

##Install relevant libraries and executable files

(1)GCC(7.4.0 of mine)
Before install high version of GCC that supports c++11
you should 1st install "gmp"   (6.1.2 of mine, no other dependencies)
	   2nd         "mpfr"  (4.0.2 of mine, depend on "gmp")
	   3rd         "mpc"   (1.1.0 of mine, depend on "gmp" and "mpfr")

and you may also need to install "binutils"(2.32 of mine) and "isl"(0.18 of mine).

If all above is OK, you can begin to install the GCC.

(2)CMake(3.15.3 of mine, binary install mode, cmake-3.15.3-linux-x86_64.tar)

(3)MPI(MPICH 3.3.1 of mine)

(4)Boost(directly copy from /export/home/wllv/mysoft/boost/boost_1_63_0)

(5)Eigen(directly copy from /export/home/wllv/mysoft/eigen3.3)

(6)Nlopt(2.6.1 of mine)

##Set cmake
Using cmake to compile the executable files "weibo", "apaweibo" and "mo-weibo" from the source codes folder apaweibo that is decompressioned from apaweibo.tgz

Some environment variables should be setted in cmake-gui, e.g.

Eigen3_DIR=/export/home/lichunqiao/Software/eigen3.3/share/eigen3/cmake
NLOPT_PATH=/export/home/lichunqiao/Software/NLOPT
Boost_INCLUDE_DIR=/export/home/lichunqiao/Software/boost_1_63_0/include
Boost_LIBRARY_DIR_DEBUG=/export/home/lichunqiao/Software/boost_1_63_0/lib
Boost_LIBRARY_DIR_RELEASE=/export/home/lichunqiao/Software/boost_1_63_0/lib
CMAKE_INSTALL_PREFIX=/export/home/lichunqiao/Documents/Wllv-software

##Check
After compiling the executable files, you can check if it is ok through the examples in the directory of "apaweibo/examples". But before that, the "conf" in the "apaweibo/examples/" should be revised.
