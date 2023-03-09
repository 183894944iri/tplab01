# tplab01
Выполнила Черникова Ирина ИУ8-23
1. Установка бибилиотеки:               wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
2. Разархивация:         tar -xzf boost_1_69_0.tar.gz
3. Подсчет количества файлов в директории ~/boost_1_69_0 не включая вложенные директории: tree -aL 1
    7 directories, 12 files
4. Подсчет количества файлов в директории ~/boost_1_69_0 включая вложенные директории:  tree -a
   5638 directories, 61191 files 
5. Подсчет количества заголовочных файлов, файлов с расширением .cpp, остальных файлов (не заголовочных и не .cpp):  
    ~ Заголовочные файлы с раширениями .h b .hpp : find . -type f -name "*.h" | wc -l      (296)
    
    find . -type f -name "*.hpp" | wc -l     (14912)
    Суммарно 15208
    
    ~ Файлы с расширением .cpp: find . -type f -name "*.cpp" | wc -l    (13774)
    
    ~ Все остальные файлы: find . -not -name "*.h" -not -name "*.hpp" -not -name "*.cpp" -not -type d|wc -l      (32209)
    
6. Полный путь: find $PWD -name any.hpp 
~   /Users/mac/boost_1_69_0/boost/fusion/include/any.hpp

/Users/mac/boost_1_69_0/boost/fusion/algorithm/query/any.hpp

/Users/mac/boost_1_69_0/boost/fusion/algorithm/query/detail/any.hpp

/Users/mac/boost_1_69_0/boost/spirit/home/support/algorithm/any.hpp

/Users/mac/boost_1_69_0/boost/proto/detail/any.hpp

/Users/mac/boost_1_69_0/boost/type_erasure/any.hpp

/Users/mac/boost_1_69_0/boost/hana/fwd/any.hpp

/Users/mac/boost_1_69_0/boost/hana/any.hpp

/Users/mac/boost_1_69_0/boost/any.hpp

/Users/mac/boost_1_69_0/boost/xpressive/detail/utility/any.hpp  

7.  grep -rl 'boost::asio'
8.  cd tools/build
  
./bootstrap.sh

./b2 install --prefix=test


...updated 436 targets...

9.   mkdir ~/boost-lib

mv -i test ~/boost-lib

10. du -ah


11. build % find . -xdev -type f -not -type d -print | xargs ls -lh | sort -k5,5 -h -r | head



