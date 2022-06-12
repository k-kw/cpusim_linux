# Cplus_sim

## Overview
光の伝搬をシミュレーションするための，main関数とヘッダを格納しています．

## Detail
main.cppがmain関数です．

cplus_hがヘッダをまとめたディレクトリで，includeすると使えますが，Dllandlibリポジトリの対応するDLLとlibを適切に配置する必要があります．以下に対応関係を示します．
##### ----対応関係----

Bmp_class_dll.h : Dllandlib/bmp_dll_ver2

complex_array_class_dll.h : Dllandlib/complexarray_ver2

#### ----対応関係----
DllandlibのREADME.mdに，各DLLが持つ機能の概略がありますので詳細はそちらをご覧ください．

main.cppにあるとおりopencvを使っています．ほかにもcomplex_array_class_dll.h : Dllandlib/complexarray_ver2/complex_array_class_dll.cppにあるとおりfftwを使っています．

cplus_sは使う必要がないです．

garbageディレクトリ内のソースファイルも，使う必要がないです．

