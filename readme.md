# 目次

- [1. 区間加算](#1-区間加算)
  - [区間和](#区間和)
  - [区間最大値](#区間最大値)
  - [区間最小値](#区間最小値)
  - [区間最大値とその個数](#区間最大値とその個数)
  - [区間最小値とその個数](#区間最小値とその個数)
  - [区間最大値とその位置](#区間最大値とその位置)
  - [区間最小値とその位置](#区間最小値とその位置)
  - [区間二乗和](#区間二乗和)
  - [区間 k 乗和 (k = 0..K)](#区間-k-乗和-k--0k)
  - [固定重み付き和 Σ w_i x_i](#固定重み付き和-σ-w_i-x_i)
  - [区間 GCD](#区間-gcd)
  - [区間和・区間最大値](#区間和区間最大値)
  - [区間和・区間最小値](#区間和区間最小値)
  - [区間和・区間二乗和](#区間和区間二乗和)
  - [区間和・区間 GCD](#区間和区間-gcd)
  - [区間最大値・区間最小値](#区間最大値区間最小値)
  - [区間最大値・区間二乗和](#区間最大値区間二乗和)
  - [区間最大値・区間 GCD](#区間最大値区間-gcd)
  - [区間最小値・区間二乗和](#区間最小値区間二乗和)
  - [区間最小値・区間 GCD](#区間最小値区間-gcd)
  - [区間二乗和・区間 GCD](#区間二乗和区間-gcd)
  - [区間和・区間最大値・区間最小値](#区間和区間最大値区間最小値)
  - [区間和・区間最大値・区間二乗和](#区間和区間最大値区間二乗和)
  - [区間和・区間最大値・区間 GCD](#区間和区間最大値区間-gcd)
  - [区間和・区間最小値・区間二乗和](#区間和区間最小値区間二乗和)
  - [区間和・区間最小値・区間 GCD](#区間和区間最小値区間-gcd)
  - [区間和・区間二乗和・区間 GCD](#区間和区間二乗和区間-gcd)
  - [区間最大値・区間最小値・区間二乗和](#区間最大値区間最小値区間二乗和)
  - [区間最大値・区間最小値・区間 GCD](#区間最大値区間最小値区間-gcd)
  - [区間最大値・区間二乗和・区間 GCD](#区間最大値区間二乗和区間-gcd)
  - [区間最小値・区間二乗和・区間 GCD](#区間最小値区間二乗和区間-gcd)
  - [区間和・区間最大値・区間最小値・区間二乗和](#区間和区間最大値区間最小値区間二乗和)
  - [区間和・区間最大値・区間最小値・区間 GCD](#区間和区間最大値区間最小値区間-gcd)
  - [区間和・区間最大値・区間二乗和・区間 GCD](#区間和区間最大値区間二乗和区間-gcd)
  - [区間和・区間最小値・区間二乗和・区間 GCD](#区間和区間最小値区間二乗和区間-gcd)
  - [区間最大値・区間最小値・区間二乗和・区間 GCD](#区間最大値区間最小値区間二乗和区間-gcd)
  - [区間和・区間最大値・区間最小値・区間二乗和・区間 GCD](#区間和区間最大値区間最小値区間二乗和区間-gcd)
  - [区間最小値と個数・区間最大値と個数](#区間最小値と個数区間最大値と個数)
  - [2 つの数列への区間加算 + 区間積和 Σ a_i b_i](#2-つの数列への区間加算--区間積和-σ-a_i-b_i)
  - [ローリングハッシュ（回文判定つき）](#ローリングハッシュ回文判定つき)
  - [歴史的最大値（過去に取った値の最大）](#歴史的最大値過去に取った値の最大)
  - [歴史的最小値（過去に取った値の最小）](#歴史的最小値過去に取った値の最小)
  - [歴史和（各時刻の値の合計）](#歴史和各時刻の値の合計)
  - [max_{a<=b<=c} (x_a - 2x_b + x_c)（オイラーツアー上の木の直径）](#max_abc-x_a---2x_b--x_cオイラーツアー上の木の直径)
  - [Σ Fib(x_i)](#σ-fibx_i)
  - [Σ R^(x_i)](#σ-rx_i)
  - [Σ sin(x_i), Σ cos(x_i)](#σ-sinx_i-σ-cosx_i)
  - [基本対称式（k 個選んだ積の総和, k = 0..K）](#基本対称式k-個選んだ積の総和-k--0k)
  - [2 つの数列への区間加算 + max(a_i + b_i), max_{i<=j}(a_i + b_j)](#2-つの数列への区間加算--maxa_i--b_i-max_ija_i--b_j)
  - [覆われている長さ（座標圧縮つき, 長方形の和集合の面積）](#覆われている長さ座標圧縮つき-長方形の和集合の面積)
  - [Σ A^(x_i)（A は固定の行列）](#σ-ax_ia-は固定の行列)
- [2. 区間更新（代入）](#2-区間更新代入)
  - [区間和](#区間和-1)
  - [区間最大値](#区間最大値-1)
  - [区間最小値](#区間最小値-1)
  - [区間最大値とその個数](#区間最大値とその個数-1)
  - [区間最小値とその個数](#区間最小値とその個数-1)
  - [区間最大値とその位置](#区間最大値とその位置-1)
  - [区間最小値とその位置](#区間最小値とその位置-1)
  - [区間二乗和](#区間二乗和-1)
  - [区間 k 乗和 (k = 0..K)](#区間-k-乗和-k--0k-1)
  - [固定重み付き和 Σ w_i x_i](#固定重み付き和-σ-w_i-x_i-1)
  - [区間積 (mod)](#区間積-mod)
  - [区間 XOR 和](#区間-xor-和)
  - [区間 AND・OR](#区間-andor)
  - [区間 GCD](#区間-gcd-1)
  - [区間最大部分和（空でない連続部分列）](#区間最大部分和空でない連続部分列)
  - [区間最小部分和（空でない連続部分列）](#区間最小部分和空でない連続部分列)
  - [区間和・区間最大値](#区間和区間最大値-1)
  - [区間和・区間最小値](#区間和区間最小値-1)
  - [区間和・区間二乗和](#区間和区間二乗和-1)
  - [区間和・区間 GCD](#区間和区間-gcd-1)
  - [区間最大値・区間最小値](#区間最大値区間最小値-1)
  - [区間最大値・区間二乗和](#区間最大値区間二乗和-1)
  - [区間最大値・区間 GCD](#区間最大値区間-gcd-1)
  - [区間最小値・区間二乗和](#区間最小値区間二乗和-1)
  - [区間最小値・区間 GCD](#区間最小値区間-gcd-1)
  - [区間二乗和・区間 GCD](#区間二乗和区間-gcd-1)
  - [区間和・区間最大値・区間最小値](#区間和区間最大値区間最小値-1)
  - [区間和・区間最大値・区間二乗和](#区間和区間最大値区間二乗和-1)
  - [区間和・区間最大値・区間 GCD](#区間和区間最大値区間-gcd-1)
  - [区間和・区間最小値・区間二乗和](#区間和区間最小値区間二乗和-1)
  - [区間和・区間最小値・区間 GCD](#区間和区間最小値区間-gcd-1)
  - [区間和・区間二乗和・区間 GCD](#区間和区間二乗和区間-gcd-1)
  - [区間最大値・区間最小値・区間二乗和](#区間最大値区間最小値区間二乗和-1)
  - [区間最大値・区間最小値・区間 GCD](#区間最大値区間最小値区間-gcd-1)
  - [区間最大値・区間二乗和・区間 GCD](#区間最大値区間二乗和区間-gcd-1)
  - [区間最小値・区間二乗和・区間 GCD](#区間最小値区間二乗和区間-gcd-1)
  - [区間和・区間最大値・区間最小値・区間二乗和](#区間和区間最大値区間最小値区間二乗和-1)
  - [区間和・区間最大値・区間最小値・区間 GCD](#区間和区間最大値区間最小値区間-gcd-1)
  - [区間和・区間最大値・区間二乗和・区間 GCD](#区間和区間最大値区間二乗和区間-gcd-1)
  - [区間和・区間最小値・区間二乗和・区間 GCD](#区間和区間最小値区間二乗和区間-gcd-1)
  - [区間最大値・区間最小値・区間二乗和・区間 GCD](#区間最大値区間最小値区間二乗和区間-gcd-1)
  - [区間和・区間最大値・区間最小値・区間二乗和・区間 GCD](#区間和区間最大値区間最小値区間二乗和区間-gcd-1)
  - [区間最小値と個数・区間最大値と個数](#区間最小値と個数区間最大値と個数-1)
  - [区間和・区間 XOR 和](#区間和区間-xor-和)
  - [ローリングハッシュ（回文判定つき）](#ローリングハッシュ回文判定つき-1)
  - [区間の関数合成（一次関数の代入 + 区間合成）](#区間の関数合成一次関数の代入--区間合成)
  - [区間の行列積（行列の代入 + 区間積）](#区間の行列積行列の代入--区間積)
  - [区間に現れる値の集合（値域が 64 以下）](#区間に現れる値の集合値域が-64-以下)
  - [区間和・最大値・最小値・二乗和・GCD・XOR・積・OR・AND](#区間和最大値最小値二乗和gcdxor積orand)
  - [区間 LCM](#区間-lcm)
  - [区間 GCD・LCM](#区間-gcdlcm)
  - [両方向の関数合成（一次関数の代入 + 左から・右からの合成, HLD 用）](#両方向の関数合成一次関数の代入--左から右からの合成-hld-用)
  - [任意のモノイドの代入 + 区間積（例: クランプ関数の合成）](#任意のモノイドの代入--区間積例-クランプ関数の合成)
- [3. 区間加算 + 区間更新](#3-区間加算--区間更新)
  - [区間和](#区間和-2)
  - [区間最大値](#区間最大値-2)
  - [区間最小値](#区間最小値-2)
  - [区間最大値とその個数](#区間最大値とその個数-2)
  - [区間最小値とその個数](#区間最小値とその個数-2)
  - [区間最大値とその位置](#区間最大値とその位置-2)
  - [区間最小値とその位置](#区間最小値とその位置-2)
  - [区間二乗和](#区間二乗和-2)
  - [区間 GCD](#区間-gcd-2)
  - [区間和・区間最大値](#区間和区間最大値-2)
  - [区間和・区間最小値](#区間和区間最小値-2)
  - [区間和・区間二乗和](#区間和区間二乗和-2)
  - [区間和・区間 GCD](#区間和区間-gcd-2)
  - [区間最大値・区間最小値](#区間最大値区間最小値-2)
  - [区間最大値・区間二乗和](#区間最大値区間二乗和-2)
  - [区間最大値・区間 GCD](#区間最大値区間-gcd-2)
  - [区間最小値・区間二乗和](#区間最小値区間二乗和-2)
  - [区間最小値・区間 GCD](#区間最小値区間-gcd-2)
  - [区間二乗和・区間 GCD](#区間二乗和区間-gcd-2)
  - [区間和・区間最大値・区間最小値](#区間和区間最大値区間最小値-2)
  - [区間和・区間最大値・区間二乗和](#区間和区間最大値区間二乗和-2)
  - [区間和・区間最大値・区間 GCD](#区間和区間最大値区間-gcd-2)
  - [区間和・区間最小値・区間二乗和](#区間和区間最小値区間二乗和-2)
  - [区間和・区間最小値・区間 GCD](#区間和区間最小値区間-gcd-2)
  - [区間和・区間二乗和・区間 GCD](#区間和区間二乗和区間-gcd-2)
  - [区間最大値・区間最小値・区間二乗和](#区間最大値区間最小値区間二乗和-2)
  - [区間最大値・区間最小値・区間 GCD](#区間最大値区間最小値区間-gcd-2)
  - [区間最大値・区間二乗和・区間 GCD](#区間最大値区間二乗和区間-gcd-2)
  - [区間最小値・区間二乗和・区間 GCD](#区間最小値区間二乗和区間-gcd-2)
  - [区間和・区間最大値・区間最小値・区間二乗和](#区間和区間最大値区間最小値区間二乗和-2)
  - [区間和・区間最大値・区間最小値・区間 GCD](#区間和区間最大値区間最小値区間-gcd-2)
  - [区間和・区間最大値・区間二乗和・区間 GCD](#区間和区間最大値区間二乗和区間-gcd-2)
  - [区間和・区間最小値・区間二乗和・区間 GCD](#区間和区間最小値区間二乗和区間-gcd-2)
  - [区間最大値・区間最小値・区間二乗和・区間 GCD](#区間最大値区間最小値区間二乗和区間-gcd-2)
  - [区間和・区間最大値・区間最小値・区間二乗和・区間 GCD](#区間和区間最大値区間最小値区間二乗和区間-gcd-2)
  - [区間最小値と個数・区間最大値と個数](#区間最小値と個数区間最大値と個数-2)
  - [隣接要素の大小（上昇・下降の個数 / ソート済み判定）](#隣接要素の大小上昇下降の個数--ソート済み判定)
  - [連続する同じ値のまとまりの個数（ランの数）](#連続する同じ値のまとまりの個数ランの数)
  - [同じ値が連続する最長の長さ](#同じ値が連続する最長の長さ)
  - [最長の狭義単調増加な連続部分列の長さ](#最長の狭義単調増加な連続部分列の長さ)
  - [max_{i<=j} (x_j - x_i)](#max_ij-x_j---x_i)
  - [異なる 2 要素の和の最大 max_{i<j} (x_i + x_j)](#異なる-2-要素の和の最大-max_ij-x_i--x_j)
  - [隣接差の絶対値の和 Σ|x_{i+1} - x_i|](#隣接差の絶対値の和-σx_i1---x_i)
  - [隣接差の絶対値の最大 max|x_{i+1} - x_i|](#隣接差の絶対値の最大-maxx_i1---x_i)
  - [区間最大値・2 番目の最大値とその個数](#区間最大値2-番目の最大値とその個数)
  - [固定オフセット付き最小値 min(x_i + c_i)](#固定オフセット付き最小値-minx_i--c_i)
  - [上位 K 個の値（重複込み）](#上位-k-個の値重複込み)
  - [歴史的最大値](#歴史的最大値)
  - [歴史的最小値](#歴史的最小値)
  - [値を M で割った余りごとの個数・区間和](#値を-m-で割った余りごとの個数区間和)
  - [全ての連続部分列の和の総和](#全ての連続部分列の和の総和)
  - [区間最大値・最小値とその個数・位置](#区間最大値最小値とその個数位置)
- [4. 区間乗算・区間アフィン変換 (x ← ax + b)](#4-区間乗算区間アフィン変換-x--ax--b)
  - [区間乗算 + 区間和 (mod)](#区間乗算--区間和-mod)
  - [区間乗算 + 区間 k 乗和 (mod)](#区間乗算--区間-k-乗和-mod)
  - [区間乗算 + 区間積 (mod)](#区間乗算--区間積-mod)
  - [区間乗算 + 区間積・素因数の集合（積のオイラー関数）](#区間乗算--区間積素因数の集合積のオイラー関数)
  - [区間乗算 + 区間 GCD](#区間乗算--区間-gcd)
  - [区間乗算 + 区間最大部分和・最小部分和](#区間乗算--区間最大部分和最小部分和)
  - [区間乗算 + 区間最小値・最大値（負の数もかけられる）](#区間乗算--区間最小値最大値負の数もかけられる)
  - [区間乗算 + 区間和・最小値・最大値](#区間乗算--区間和最小値最大値)
  - [区間アフィン + 区間和 (mod)](#区間アフィン--区間和-mod)
  - [区間アフィン + 区間二乗和 (mod)](#区間アフィン--区間二乗和-mod)
  - [区間アフィン + 区間 k 乗和 (mod)](#区間アフィン--区間-k-乗和-mod)
  - [区間アフィン + 固定重み付き和 Σ w_i x_i (mod)](#区間アフィン--固定重み付き和-σ-w_i-x_i-mod)
  - [区間アフィン + 区間 GCD](#区間アフィン--区間-gcd)
  - [区間アフィン + 区間最小値・最大値（a は負でもよい）](#区間アフィン--区間最小値最大値a-は負でもよい)
  - [区間アフィン + 区間和・最小値・最大値](#区間アフィン--区間和最小値最大値)
  - [区間アフィン + 区間最小値と個数・最大値と個数](#区間アフィン--区間最小値と個数最大値と個数)
  - [区間アフィン + 区間最小値の位置・最大値の位置](#区間アフィン--区間最小値の位置最大値の位置)
  - [区間アフィン + ローリングハッシュ（回文判定つき）](#区間アフィン--ローリングハッシュ回文判定つき)
  - [区間アフィン + 隣接積和 Σ x_i x_{i+1} (mod)](#区間アフィン--隣接積和-σ-x_i-x_i1-mod)
  - [2 つの数列への区間アフィン + 区間積和 Σ a_i b_i](#2-つの数列への区間アフィン--区間積和-σ-a_i-b_i)
  - [点の回転・反転・平行移動 + 座標の和・バウンディングボックス](#点の回転反転平行移動--座標の和バウンディングボックス)
  - [区間乗算 + 区間和・最小値・最大値・二乗和・GCD](#区間乗算--区間和最小値最大値二乗和gcd)
  - [区間アフィン + 区間和・最小値・最大値・二乗和・GCD](#区間アフィン--区間和最小値最大値二乗和gcd)
  - [区間乗算 + 区間 GCD・LCM](#区間乗算--区間-gcdlcm)
  - [区間乗算 + 区間 LCM](#区間乗算--区間-lcm)
  - [区間乗算 + 区間最小値・最大値とその個数・位置](#区間乗算--区間最小値最大値とその個数位置)
- [5. 区間 chmin / chmax](#5-区間-chmin--chmax)
  - [区間 chmin + 区間最大値](#区間-chmin--区間最大値)
  - [区間 chmin + 区間最小値](#区間-chmin--区間最小値)
  - [区間 chmin + 区間最小値とその個数](#区間-chmin--区間最小値とその個数)
  - [区間 chmin + 区間最小値・最大値](#区間-chmin--区間最小値最大値)
  - [区間 chmin + 区間最小値の位置](#区間-chmin--区間最小値の位置)
  - [区間 chmax + 区間最大値](#区間-chmax--区間最大値)
  - [区間 chmax + 区間最小値](#区間-chmax--区間最小値)
  - [区間 chmax + 区間最大値とその個数](#区間-chmax--区間最大値とその個数)
  - [区間 chmax + 区間最小値・最大値](#区間-chmax--区間最小値最大値)
  - [区間 chmax + 区間最大値の位置](#区間-chmax--区間最大値の位置)
  - [区間加算・chmin・chmax・代入 + 区間最小値・最大値](#区間加算chminchmax代入--区間最小値最大値)
  - [区間 chmin + 区間最小値とその個数・位置・最大値](#区間-chmin--区間最小値とその個数位置最大値)
  - [区間 chmax + 区間最大値とその個数・位置・最小値](#区間-chmax--区間最大値とその個数位置最小値)
  - [区間アフィン・chmin・chmax・代入 + 区間最小値・最大値](#区間アフィンchminchmax代入--区間最小値最大値)
- [6. 区間に添字の関数を加算・代入](#6-区間に添字の関数を加算代入)
  - [等差数列加算 + 区間和](#等差数列加算--区間和)
  - [等差数列加算・等差数列代入 + 区間和](#等差数列加算等差数列代入--区間和)
  - [等差数列代入 + 区間和・最小値・最大値](#等差数列代入--区間和最小値最大値)
  - [二次式加算 + 区間和 (mod)](#二次式加算--区間和-mod)
  - [等比数列加算 + 区間和 (mod)](#等比数列加算--区間和-mod)
  - [フィボナッチ数列加算 + 区間和 (mod)](#フィボナッチ数列加算--区間和-mod)
  - [等差数列加算 + 区間二乗和 (mod)](#等差数列加算--区間二乗和-mod)
  - [任意の基底関数の線形結合を加算 + 区間和 (mod)](#任意の基底関数の線形結合を加算--区間和-mod)
  - [等差数列加算・等差数列代入 + 等差数列判定・公差・区間 GCD](#等差数列加算等差数列代入--等差数列判定公差区間-gcd)
  - [添字の偶奇で別々に加算 + 偶奇別の和・最大値](#添字の偶奇で別々に加算--偶奇別の和最大値)
  - [任意の基底関数の線形結合を加算・代入 + 区間和 (mod)](#任意の基底関数の線形結合を加算代入--区間和-mod)
- [7. 区間符号反転 (x ← -x)](#7-区間符号反転-x---x)
  - [区間和・最小値・最大値](#区間和最小値最大値)
  - [区間最大部分和・最小部分和](#区間最大部分和最小部分和)
  - [区間最小値と個数・最大値と個数](#区間最小値と個数最大値と個数)
  - [区間最小値の位置・最大値の位置](#区間最小値の位置最大値の位置)
  - [区間和・最小値・最大値とその個数・位置・最大部分和・最小部分和](#区間和最小値最大値とその個数位置最大部分和最小部分和)
  - [区間積・GCD・LCM](#区間積gcdlcm)
- [8. 区間 0/1 反転・代入](#8-区間-01-反転代入)
  - [反転 + 1 の個数](#反転--1-の個数)
  - [反転 + 転倒数](#反転--転倒数)
  - [反転 + 最長連続 0 / 1](#反転--最長連続-0--1)
  - [反転・代入 + 1 の個数・転倒数・最長連続 0 / 1](#反転代入--1-の個数転倒数最長連続-0--1)
  - [反転・代入 + ローリングハッシュ（回文判定つき）](#反転代入--ローリングハッシュ回文判定つき)
  - [反転・代入 + ランの数・最長の交互列 (0101...)](#反転代入--ランの数最長の交互列-0101)
  - [反転・代入 + 最長の広義単調部分列（連続でなくてよい）](#反転代入--最長の広義単調部分列連続でなくてよい)
  - [反転・代入 + 1 の個数・1 の位置の和](#反転代入--1-の個数1-の位置の和)
- [9. 区間の値の置換（値域が小さいとき）](#9-区間の値の置換値域が小さいとき)
  - [x ← to[x] + 各値の個数・区間和](#x--tox--各値の個数区間和)
  - [x ← to[x] + 転倒数](#x--tox--転倒数)
  - [x ← to[x] + ローリングハッシュ（回文判定つき）](#x--tox--ローリングハッシュ回文判定つき)
  - [x ← (x + f) mod M + 各値の個数・区間和](#x--x--f-mod-m--各値の個数区間和)
  - [x ← to[x] + 隣接する値の組 (u, v) の個数](#x--tox--隣接する値の組-u-v-の個数)
- [10. 状態付きの値](#10-状態付きの値)
  - [状態の反転・状態別の加算 + 状態別の最大値・和・個数](#状態の反転状態別の加算--状態別の最大値和個数)
- [11. 区間ビット演算 (AND / OR / XOR)](#11-区間ビット演算-and--or--xor)
  - [XOR + 区間 XOR 和](#xor--区間-xor-和)
  - [AND・OR・代入 + 区間 OR・AND](#andor代入--区間-orand)
  - [AND・OR・XOR・代入 + 区間和・OR・AND・XOR・popcount](#andorxor代入--区間和orandxorpopcount)
  - [左シフト (×2^k) + 区間和・最大値・最小値・OR・AND・XOR・GCD・LCM](#左シフト-2k--区間和最大値最小値orandxorgcdlcm)
- [12. 括弧列](#12-括弧列)
  - [反転 + 正しい括弧列判定](#反転--正しい括弧列判定)
  - [反転・代入 + 正しい括弧列判定](#反転代入--正しい括弧列判定)
  - [反転・代入 + 対応の取れる括弧のペア数（最長の正しい括弧部分列）](#反転代入--対応の取れる括弧のペア数最長の正しい括弧部分列)
- [13. 区間行列作用（線形作用の一般化）](#13-区間行列作用線形作用の一般化)
  - [ベクトルの和 + 行列作用 (mod)](#ベクトルの和--行列作用-mod)

# 1. 区間加算

## 区間和

```cpp
struct S{long long sum; long long len;};
using F=long long;
S op(S a,S b){return {a.sum+b.sum,a.len+b.len};}
S e(){return {0,0};}
S mapping(F f,S x){return {x.sum+f*x.len,x.len};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum
// 巨大な配列: 座標圧縮して 1 要素を長さ len の区間にする (初期値 {0, 区間の長さ})
```

## 区間最大値

```cpp
const long long INF=1e18;
using S=long long;
using F=long long;
S op(S a,S b){return std::max(a,b);}
S e(){return -INF;}
S mapping(F f,S x){return f+x;}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 取得: 最大値 = seg.prod(l,r)
// x_i >= K となる最左の i (l 以降): seg.max_right(l,[&](S v){return v<K;})
```

## 区間最小値

```cpp
const long long INF=1e18;
using S=long long;
using F=long long;
S op(S a,S b){return std::min(a,b);}
S e(){return INF;}
S mapping(F f,S x){return f+x;}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 取得: 最小値 = seg.prod(l,r)
```

## 区間最大値とその個数

```cpp
const long long INF=1e18;
struct S{long long mx; long long cnt;};
using F=long long;
S op(S a,S b){
    if(a.mx>b.mx) return a;
    if(a.mx<b.mx) return b;
    return {a.mx,a.cnt+b.cnt};
}
S e(){return {-INF,0};}
S mapping(F f,S x){return {x.mx+f,x.cnt};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 個数 = p.cnt
```

## 区間最小値とその個数

```cpp
const long long INF=1e18;
struct S{long long mn; long long cnt;};
using F=long long;
S op(S a,S b){
    if(a.mn<b.mn) return a;
    if(a.mn>b.mn) return b;
    return {a.mn,a.cnt+b.cnt};
}
S e(){return {INF,0};}
S mapping(F f,S x){return {x.mn+f,x.cnt};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 個数 = p.cnt
// 常に x_i >= 0 なら 0 の個数 = (mn==0 ? cnt : 0)  (長方形の和集合の面積など)
```

## 区間最大値とその位置

```cpp
const long long INF=1e18;
struct S{long long mx; int idx;};
using F=long long;
S op(S a,S b){return a.mx>=b.mx?a:b;}  // 最左 (最右なら >)
S e(){return {-INF,-1};}
S mapping(F f,S x){return {x.mx+f,x.idx};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, i}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最左位置 = p.idx
```

## 区間最小値とその位置

```cpp
const long long INF=1e18;
struct S{long long mn; int idx;};
using F=long long;
S op(S a,S b){return a.mn<=b.mn?a:b;}  // 最左 (最右なら <)
S e(){return {INF,-1};}
S mapping(F f,S x){return {x.mn+f,x.idx};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最左位置 = p.idx
```

## 区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint sum; mint sq; mint len;};
using F=mint;
S op(S a,S b){return {a.sum+b.sum,a.sq+b.sq,a.len+b.len};}
S e(){return {0,0,0};}
S mapping(F f,S x){return {x.sum+f*x.len,x.sq+2*f*x.sum+f*f*x.len,x.len};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 二乗和 = p.sq, 和 = p.sum
// 分散: sq/len - (sum/len)^2,  Σ_{i<j} x_i x_j = (sum^2 - sq) / 2
```

## 区間 k 乗和 (k = 0..K)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const int K=3;
struct S{mint p[K+1];};  // p[j] = Σ x_i^j  (p[0] = 長さ)
using F=mint;
S op(S a,S b){for(int j=0;j<=K;j++) a.p[j]+=b.p[j]; return a;}
S e(){return S{};}
S mapping(F f,S x){
    static mint C[K+1][K+1];
    if(C[0][0]==0) for(int i=0;i<=K;i++){C[i][0]=1; for(int j=1;j<=i;j++) C[i][j]=C[i-1][j-1]+C[i-1][j];}
    mint fp[K+1]; fp[0]=1;
    for(int j=1;j<=K;j++) fp[j]=fp[j-1]*f;
    S r{};
    for(int k=0;k<=K;k++) for(int j=0;j<=k;j++) r.p[k]+=C[k][j]*fp[k-j]*x.p[j];
    return r;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: p[j] = a_i^j
// 取得: auto p=seg.prod(l,r); Σ x_i^k = p.p[k]
// Σ C(x_i, 2) = (p[2] - p[1]) / 2
```

## 固定重み付き和 Σ w_i x_i

```cpp
struct S{long long wx; long long w;};
using F=long long;
S op(S a,S b){return {a.wx+b.wx,a.w+b.w};}
S e(){return {0,0};}
S mapping(F f,S x){return {x.wx+f*x.w,x.w};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {w_i*a_i, w_i}
// 取得: auto p=seg.prod(l,r); Σ w_i x_i = p.wx
// w_i = i で Σ i·x_i
```

## 区間 GCD

```cpp
struct S{long long l,r,g,len;};  // 左端の値, 右端の値, 隣接差の GCD
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0};}
S mapping(F f,S x){return x.len==0?x:S{x.l+f,x.r+f,x.g,x.len};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); GCD = std::gcd(std::abs(p.l), p.g), 全部等しい <=> p.g==0
```

## 区間和・区間最大値

```cpp
const long long INF=1e18;
struct S{long long sum,mx,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.len+b.len};
}
S e(){return {0,-INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sum+=f*x.len;
    x.mx+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx
```

## 区間和・区間最小値

```cpp
const long long INF=1e18;
struct S{long long sum,mn,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {0,INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sum+=f*x.len;
    x.mn+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn
```

## 区間和・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.len+b.len};
}
S e(){return {0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 二乗和 = p.sq
```

## 区間和・区間 GCD

```cpp
struct S{long long sum,l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sum+=f*x.len;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最大値・区間最小値

```cpp
const long long INF=1e18;
struct S{long long mx,mn,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {-INF,INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.mx+=f;
    x.mn+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn
```

## 区間最大値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mx+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 二乗和 = p.sq
```

## 区間最大値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mx,l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {-INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.mx+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mn+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 二乗和 = p.sq
```

## 区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mn,l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.mn+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最大値・区間最小値

```cpp
const long long INF=1e18;
struct S{long long sum,mx,mn,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {0,-INF,INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sum+=f*x.len;
    x.mx+=f;
    x.mn+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn
```

## 区間和・区間最大値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mx+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 二乗和 = p.sq
```

## 区間和・区間最大値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mx,l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sum+=f*x.len;
    x.mx+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mn+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 二乗和 = p.sq
```

## 区間和・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mn,l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sum+=f*x.len;
    x.mn+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最大値・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mx+=f;
    x.mn+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq
```

## 区間最大値・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mx,mn,l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {-INF,INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.mx+=f;
    x.mn+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最大値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mx+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mn+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最大値・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mx+=f;
    x.mn+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq
```

## 区間和・区間最大値・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mx,mn,l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sum+=f*x.len;
    x.mx+=f;
    x.mn+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最大値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mx+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mn+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最大値・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mx+=f;
    x.mn+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最大値・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.sq+=2*mint(f)*x.sum+mint(f)*f*x.len;
    x.sum+=f*x.len;
    x.mx+=f;
    x.mn+=f;
    x.l+=f;
    x.r+=f;
    return x;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最小値と個数・区間最大値と個数

```cpp
const long long INF=1e18;
struct S{long long mn,mncnt,mx,mxcnt,len;};
using F=long long;
S op(S x,S y){
    S r; r.len=x.len+y.len;
    if(x.mn<y.mn) r.mn=x.mn,r.mncnt=x.mncnt;
    else if(x.mn>y.mn) r.mn=y.mn,r.mncnt=y.mncnt;
    else r.mn=x.mn,r.mncnt=x.mncnt+y.mncnt;
    if(x.mx>y.mx) r.mx=x.mx,r.mxcnt=x.mxcnt;
    else if(x.mx<y.mx) r.mx=y.mx,r.mxcnt=y.mxcnt;
    else r.mx=x.mx,r.mxcnt=x.mxcnt+y.mxcnt;
    return r;
}
S e(){return {INF,0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    return S{x.mn+f,x.mncnt,x.mx+f,x.mxcnt,x.len};
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, 1, a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (個数 p.mncnt), 最大値 = p.mx (個数 p.mxcnt)
```

## 2 つの数列への区間加算 + 区間積和 Σ a_i b_i

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint a; mint b; mint ab; mint len;};
struct F{mint p; mint q;};  // a_i += p, b_i += q
S op(S x,S y){return {x.a+y.a,x.b+y.b,x.ab+y.ab,x.len+y.len};}
S e(){return {0,0,0,0};}
S mapping(F f,S x){
    return {x.a+f.p*x.len,x.b+f.q*x.len,
            x.ab+f.p*x.b+f.q*x.a+f.p*f.q*x.len,x.len};
}
F composition(F f,F g){return {f.p+g.p,f.q+g.q};}
F id(){return {0,0};}
// 初期値: {a_i, b_i, a_i*b_i, 1}
// 取得: auto p=seg.prod(l,r); Σ a_i b_i = p.ab, Σ a_i = p.a, Σ b_i = p.b
```

## ローリングハッシュ（回文判定つき）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const mint B=1000003;
struct S{mint h,rh,pw,geo;};  // pw = B^len, geo = 1+B+...+B^(len-1)
using F=mint;
S op(S a,S b){
    return {a.h*b.pw+b.h, b.rh*a.pw+a.rh, a.pw*b.pw, a.geo*b.pw+b.geo};
}
S e(){return {0,0,1,0};}
S mapping(F f,S x){return {x.h+f*x.geo,x.rh+f*x.geo,x.pw,x.geo};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {c_i, c_i, B, 1}
// 取得: auto p=seg.prod(l,r); ハッシュ = p.h, 回文 <=> p.h==p.rh
```

## 歴史的最大値（過去に取った値の最大）

```cpp
const long long INF=1e18;
struct S{long long mx,hmx;};  // 現在の最大値, 歴史的最大値
struct F{long long add,peak;};  // 加算の合計, 途中までの加算の合計の最大
S op(S a,S b){return {std::max(a.mx,b.mx),std::max(a.hmx,b.hmx)};}
S e(){return {-INF,-INF};}
S mapping(F f,S x){return {x.mx+f.add,std::max(x.hmx,x.mx+f.peak)};}
F composition(F f,F g){return {g.add+f.add,std::max(g.peak,g.add+f.peak)};}
F id(){return {0,0};}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 歴史的最大値 = p.hmx, 現在の最大値 = p.mx
// 加算 v: {v, max(v,0)}
```

## 歴史的最小値（過去に取った値の最小）

```cpp
const long long INF=1e18;
struct S{long long mn,hmn;};  // 現在の最小値, 歴史的最小値
struct F{long long add,low;};  // 加算の合計, 途中までの加算の合計の最小
S op(S a,S b){return {std::min(a.mn,b.mn),std::min(a.hmn,b.hmn)};}
S e(){return {INF,INF};}
S mapping(F f,S x){return {x.mn+f.add,std::min(x.hmn,x.mn+f.low)};}
F composition(F f,F g){return {g.add+f.add,std::min(g.low,g.add+f.low)};}
F id(){return {0,0};}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 歴史的最小値 = p.hmn, 現在の最小値 = p.mn
// 加算 v: {v, min(v,0)}
```

## 歴史和（各時刻の値の合計）

```cpp
struct S{long long sum,hsum,len;};  // hsum: これまでの各時刻の sum の合計
struct F{long long a,t,c;};  // sum += a*len, hsum += t*sum + c*len (sum は適用前)
S op(S x,S y){return {x.sum+y.sum,x.hsum+y.hsum,x.len+y.len};}
S e(){return {0,0,0};}
S mapping(F f,S x){return {x.sum+f.a*x.len,x.hsum+f.t*x.sum+f.c*x.len,x.len};}
F composition(F f,F g){return {g.a+f.a,g.t+f.t,g.c+f.c+f.t*g.a};}
F id(){return {0,0,0};}
// 初期値: {a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 歴史和 = p.hsum, 現在の和 = p.sum
// 加算 v: {v,0,0}, 時刻を 1 進める (hsum += sum): {0,1,0}
// 長方形加算・長方形和 (オフライン): x で掃引し、y 方向の区間加算と時刻を進める操作で各時刻の和を累積する
```

## max_{a<=b<=c} (x_a - 2x_b + x_c)（オイラーツアー上の木の直径）

```cpp
const long long INF=1e18;
struct S{long long mx,mn,lm,rm,best;};
// lm = max_{a<=b}(x_a-2x_b), rm = max_{b<=c}(-2x_b+x_c), best = max_{a<=b<=c}(x_a-2x_b+x_c)
using F=long long;
S op(S p,S q){
    return {std::max(p.mx,q.mx),std::min(p.mn,q.mn),
            std::max({p.lm,q.lm,p.mx-2*q.mn}),
            std::max({p.rm,q.rm,q.mx-2*p.mn}),
            std::max({p.best,q.best,p.lm+q.mx,p.mx+q.rm})};
}
S e(){return {-INF,INF,-INF,-INF,-INF};}
S mapping(F f,S x){
    if(x.mx<x.mn) return x;
    return {x.mx+f,x.mn+f,x.lm-f,x.rm-f,x.best};
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, -a_i, -a_i, 0}
// 取得: auto p=seg.prod(l,r); max (x_a - 2x_b + x_c) = p.best
// 深さ列 (オイラーツアー) に辺の重み変更 = 部分木の区間加算 → best が直径
```

## Σ Fib(x_i)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

struct S{mint f0,f1;};  // Σ Fib(x_i), Σ Fib(x_i+1)
struct F{mint a,b;};  // 加算 v: {Fib(v), Fib(v+1)}
S op(S x,S y){return {x.f0+y.f0,x.f1+y.f1};}
S e(){return {0,0};}
S mapping(F f,S x){return {(f.b-f.a)*x.f0+f.a*x.f1,f.a*x.f0+f.b*x.f1};}
F composition(F f,F g){return {f.a*g.b+(f.b-f.a)*g.a,f.a*g.a+f.b*g.b};}
F id(){return {0,1};}
F make(long long v){  // {Fib(v), Fib(v+1)}, v >= 0
    F r=id(),p{1,1};
    for(;v;v>>=1,p=composition(p,p)) if(v&1) r=composition(r,p);
    return r;
}
// 初期値: F t=make(a_i); {t.a, t.b}
// 取得: auto p=seg.prod(l,r); Σ Fib(x_i) = p.f0
// 加算 v: make(v)
```

## Σ R^(x_i)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const mint R=3;
using S=mint;  // Σ R^(x_i)
using F=mint;  // 加算 v: R^v
S op(S a,S b){return a+b;}
S e(){return 0;}
S mapping(F f,S x){return f*x;}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: R.pow(a_i)
// 取得: Σ R^(x_i) = seg.prod(l,r)
// 加算 v: R.pow(v)
```

## Σ sin(x_i), Σ cos(x_i)

```cpp
struct S{double s,c;};  // Σ sin x_i, Σ cos x_i
struct F{double s,c;};  // 加算 v: {sin v, cos v}
S op(S a,S b){return {a.s+b.s,a.c+b.c};}
S e(){return {0,0};}
S mapping(F f,S x){return {x.s*f.c+x.c*f.s,x.c*f.c-x.s*f.s};}
F composition(F f,F g){return {f.s*g.c+f.c*g.s,f.c*g.c-f.s*g.s};}
F id(){return {0,1};}
// 初期値: {sin a_i, cos a_i}
// 取得: auto p=seg.prod(l,r); Σ sin x_i = p.s, Σ cos x_i = p.c
```

## 基本対称式（k 個選んだ積の総和, k = 0..K）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=3;
struct S{mint e[K+1]; long long len;};  // e[k] = Σ_{i_1<...<i_k} x_{i_1}...x_{i_k}  (e[0] = 1)
using F=mint;
S op(S a,S b){
    S r{}; r.len=a.len+b.len;
    for(int i=0;i<=K;i++) for(int j=0;i+j<=K;j++) r.e[i+j]+=a.e[i]*b.e[j];
    return r;
}
S e(){S r{}; r.e[0]=1; return r;}
S mapping(F f,S x){
    S r{}; r.len=x.len;
    for(int j=0;j<=K;j++){
        mint c=1,fp=1;  // c = C(len-j, m), fp = f^m
        for(int m=0;j+m<=K;m++){
            r.e[j+m]+=c*fp*x.e[j];
            c=c*mint(x.len-j-m)/(m+1); fp*=f;
        }
    }
    return r;
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: e = {1, a_i, 0, ...}, len = 1
// 取得: auto p=seg.prod(l,r); k 個選んだ積の総和 = p.e[k]
```

## 2 つの数列への区間加算 + max(a_i + b_i), max_{i<=j}(a_i + b_j)

```cpp
const long long INF=1e18;
struct S{long long ma,mb,mab,best;};  // max a_i, max b_i, max(a_i + b_i), max_{i<=j}(a_i + b_j)
struct F{long long p,q;};  // a_i += p, b_i += q
S op(S x,S y){
    return {std::max(x.ma,y.ma),std::max(x.mb,y.mb),std::max(x.mab,y.mab),
            std::max({x.best,y.best,x.ma+y.mb})};
}
S e(){return {-INF,-INF,-INF,-INF};}
S mapping(F f,S x){
    if(x.ma==-INF) return x;
    return {x.ma+f.p,x.mb+f.q,x.mab+f.p+f.q,x.best+f.p+f.q};
}
F composition(F f,F g){return {f.p+g.p,f.q+g.q};}
F id(){return {0,0};}
// 初期値: {a_i, b_i, a_i+b_i, a_i+b_i}
// 取得: auto p=seg.prod(l,r); max a = p.ma, max b = p.mb, max(a_i + b_i) = p.mab, max_{i<=j}(a_i + b_j) = p.best
// i<j にするときは初期値の best を -INF にする
```

## 覆われている長さ（座標圧縮つき, 長方形の和集合の面積）

```cpp
const long long INF=1e18;
struct S{long long mn,cnt,len;};  // cnt: 最小値をとる部分の長さの合計, len: 長さの合計
using F=long long;
S op(S a,S b){
    long long len=a.len+b.len;
    if(a.mn<b.mn) return {a.mn,a.cnt,len};
    if(a.mn>b.mn) return {b.mn,b.cnt,len};
    return {a.mn,a.cnt+b.cnt,len};
}
S e(){return {INF,0,0};}
S mapping(F f,S x){return {x.mn+f,x.cnt,x.len};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: 座標圧縮した区間 [X_k, X_{k+1}) ごとに {0, X_{k+1}-X_k, X_{k+1}-X_k}
// 取得: auto p=seg.prod(l,r); 1 回以上覆われている長さ = p.len - (p.mn==0 ? p.cnt : 0)
// 長方形の和集合の面積: x で掃引し、y 方向の区間に +1 / -1 して、覆われている長さ × 幅 を足す
```

## Σ A^(x_i)（A は固定の行列）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=2;
using M=std::array<std::array<mint,K>,K>;
M mul(const M&a,const M&b){
    M r{};
    for(int i=0;i<K;i++) for(int k=0;k<K;k++) for(int j=0;j<K;j++) r[i][j]+=a[i][k]*b[k][j];
    return r;
}
M unit(){M r{}; for(int i=0;i<K;i++) r[i][i]=1; return r;}
M mpow(M a,long long n){M r=unit(); for(;n;n>>=1,a=mul(a,a)) if(n&1) r=mul(r,a); return r;}
using S=M;  // Σ A^(x_i)
using F=M;  // 加算 v: A^v
S op(S a,S b){for(int i=0;i<K;i++) for(int j=0;j<K;j++) a[i][j]+=b[i][j]; return a;}
S e(){return M{};}
S mapping(F f,S x){return mul(f,x);}
F composition(F f,F g){return mul(f,g);}
F id(){return unit();}
// 初期値: mpow(A, a_i)
// 取得: Σ A^(x_i) = seg.prod(l,r)
// 加算 v: mpow(A, v)
// A = {{0,1},{1,1}} で Σ Fib(x_i) = 結果の [0][1]
```

# 2. 区間更新（代入）

## 区間和

```cpp
struct S{long long sum; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){return {a.sum+b.sum,a.len+b.len};}
S e(){return {0,0};}
S mapping(F f,S x){return f==ID?x:S{f*x.len,x.len};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum
```

## 区間最大値

```cpp
const long long INF=1e18;
using S=long long;
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){return std::max(a,b);}
S e(){return -INF;}
S mapping(F f,S x){return f==ID?x:f;}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 取得: 最大値 = seg.prod(l,r)
```

## 区間最小値

```cpp
const long long INF=1e18;
using S=long long;
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){return std::min(a,b);}
S e(){return INF;}
S mapping(F f,S x){return f==ID?x:f;}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 取得: 最小値 = seg.prod(l,r)
```

## 区間最大値とその個数

```cpp
const long long INF=1e18;
struct S{long long mx; long long cnt; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.mx>b.mx) return {a.mx,a.cnt,a.len+b.len};
    if(a.mx<b.mx) return {b.mx,b.cnt,a.len+b.len};
    return {a.mx,a.cnt+b.cnt,a.len+b.len};
}
S e(){return {-INF,0,0};}
S mapping(F f,S x){return f==ID?x:S{f,x.len,x.len};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 個数 = p.cnt
```

## 区間最小値とその個数

```cpp
const long long INF=1e18;
struct S{long long mn; long long cnt; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.mn<b.mn) return {a.mn,a.cnt,a.len+b.len};
    if(a.mn>b.mn) return {b.mn,b.cnt,a.len+b.len};
    return {a.mn,a.cnt+b.cnt,a.len+b.len};
}
S e(){return {INF,0,0};}
S mapping(F f,S x){return f==ID?x:S{f,x.len,x.len};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 個数 = p.cnt
```

## 区間最大値とその位置

```cpp
const long long INF=1e18;
struct S{long long mx; int idx; int l;};  // 最大値, その最左位置, 区間の左端
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    S r=a.mx>=b.mx?a:b;
    r.l=std::min(a.l,b.l);
    return r;
}
S e(){return {-INF,INT_MAX,INT_MAX};}
S mapping(F f,S x){return f==ID?x:S{f,x.l,x.l};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, i, i}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最左位置 = p.idx
```

## 区間最小値とその位置

```cpp
const long long INF=1e18;
struct S{long long mn; int idx; int l;};  // 最小値, その最左位置, 区間の左端
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    S r=a.mn<=b.mn?a:b;
    r.l=std::min(a.l,b.l);
    return r;
}
S e(){return {INF,INT_MAX,INT_MAX};}
S mapping(F f,S x){return f==ID?x:S{f,x.l,x.l};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, i, i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最左位置 = p.idx
```

## 区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint sum; mint sq; mint len;};
using F=long long;  // 代入する値は [0, mod)
const F ID=-1;
S op(S a,S b){return {a.sum+b.sum,a.sq+b.sq,a.len+b.len};}
S e(){return {0,0,0};}
S mapping(F f,S x){
    if(f==ID) return x;
    mint v=f;
    return {v*x.len,v*v*x.len,x.len};
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 二乗和 = p.sq, 和 = p.sum
```

## 区間 k 乗和 (k = 0..K)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=3;
struct S{mint p[K+1];};  // p[j] = Σ x_i^j  (p[0] = 長さ)
using F=long long;  // 代入する値は [0, mod)
const F ID=-1;
S op(S a,S b){for(int j=0;j<=K;j++) a.p[j]+=b.p[j]; return a;}
S e(){return S{};}
S mapping(F f,S x){
    if(f==ID) return x;
    S r{}; mint v=1;
    for(int j=0;j<=K;j++){r.p[j]=v*x.p[0]; v*=f;}
    return r;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: p[j] = a_i^j
// 取得: auto p=seg.prod(l,r); Σ x_i^k = p.p[k]
```

## 固定重み付き和 Σ w_i x_i

```cpp
struct S{long long wx; long long w;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){return {a.wx+b.wx,a.w+b.w};}
S e(){return {0,0};}
S mapping(F f,S x){return f==ID?x:S{f*x.w,x.w};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {w_i*a_i, w_i}
// 取得: auto p=seg.prod(l,r); Σ w_i x_i = p.wx
```

## 区間積 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint prod; long long len;};
using F=long long;  // 代入する値は [0, mod)
const F ID=-1;
S op(S a,S b){return {a.prod*b.prod,a.len+b.len};}
S e(){return {1,0};}
S mapping(F f,S x){return f==ID?x:S{mint(f).pow(x.len),x.len};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 積 = p.prod
```

## 区間 XOR 和

```cpp
struct S{long long x; long long len;};
using F=long long;
const F ID=-1;  // 代入する値は非負
S op(S a,S b){return {a.x^b.x,a.len+b.len};}
S e(){return {0,0};}
S mapping(F f,S x){return f==ID?x:S{(x.len&1)?f:0,x.len};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); XOR = p.x
```

## 区間 AND・OR

```cpp
struct S{long long orv; long long andv;};
using F=long long;
const F ID=-1;  // 代入する値は非負
S op(S a,S b){return {a.orv|b.orv,a.andv&b.andv};}
S e(){return {0,-1};}
S mapping(F f,S x){return f==ID?x:S{f,f};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); OR = p.orv, AND = p.andv
```

## 区間 GCD

```cpp
using S=long long;
using F=long long;
const F ID=-1;  // 代入する値は非負
S op(S a,S b){return std::gcd(a,b);}
S e(){return 0;}
S mapping(F f,S x){return f==ID?x:f;}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 取得: GCD = seg.prod(l,r)
```

## 区間最大部分和（空でない連続部分列）

```cpp
const long long INF=1e18;
struct S{long long sum,pre,suf,best,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    return {a.sum+b.sum,
            std::max(a.pre,a.sum+b.pre),
            std::max(b.suf,b.sum+a.suf),
            std::max({a.best,b.best,a.suf+b.pre}),
            a.len+b.len};
}
S e(){return {0,-INF,-INF,-INF,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    long long v=f>=0?f*x.len:f;
    return {f*x.len,v,v,v,x.len};
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大部分和 = p.best, 最大 prefix 和 = p.pre, 最大 suffix 和 = p.suf
// 空を許すなら max(best,0)。pre: 最大の prefix 和, suf: 最大の suffix 和
```

## 区間最小部分和（空でない連続部分列）

```cpp
const long long INF=1e18;
struct S{long long sum,pre,suf,best,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    return {a.sum+b.sum,
            std::min(a.pre,a.sum+b.pre),
            std::min(b.suf,b.sum+a.suf),
            std::min({a.best,b.best,a.suf+b.pre}),
            a.len+b.len};
}
S e(){return {0,INF,INF,INF,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    long long v=f<=0?f*x.len:f;
    return {f*x.len,v,v,v,x.len};
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 最小部分和 = p.best, 最小 prefix 和 = p.pre, 最小 suffix 和 = p.suf
```

## 区間和・区間最大値

```cpp
const long long INF=1e18;
struct S{long long sum,mx,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.len+b.len};
}
S e(){return {0,-INF,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx
```

## 区間和・区間最小値

```cpp
const long long INF=1e18;
struct S{long long sum,mn,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {0,INF,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mn=f;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn
```

## 区間和・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.len+b.len};
}
S e(){return {0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.sq=mint(f)*f*x.len;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 二乗和 = p.sq
```

## 区間和・区間 GCD

```cpp
struct S{long long sum,l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最大値・区間最小値

```cpp
const long long INF=1e18;
struct S{long long mx,mn,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {-INF,INF,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.mx=f;
    x.mn=f;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn
```

## 区間最大値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.sq=mint(f)*f*x.len;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 二乗和 = p.sq
```

## 区間最大値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mx,l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {-INF,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.mx=f;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,INF,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mn=f;
    x.sq=mint(f)*f*x.len;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 二乗和 = p.sq
```

## 区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mn,l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {INF,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.mn=f;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.sq=mint(f)*f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最大値・区間最小値

```cpp
const long long INF=1e18;
struct S{long long sum,mx,mn,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {0,-INF,INF,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.mn=f;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn
```

## 区間和・区間最大値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.sq=mint(f)*f*x.len;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 二乗和 = p.sq
```

## 区間和・区間最大値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mx,l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,INF,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mn=f;
    x.sq=mint(f)*f*x.len;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 二乗和 = p.sq
```

## 区間和・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mn,l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mn=f;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.sq=mint(f)*f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最大値・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,INF,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.mn=f;
    x.sq=mint(f)*f*x.len;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq
```

## 区間最大値・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mx,mn,l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {-INF,INF,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.mx=f;
    x.mn=f;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最大値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.sq=mint(f)*f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mn=f;
    x.sq=mint(f)*f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最大値・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,INF,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.mn=f;
    x.sq=mint(f)*f*x.len;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq
```

## 区間和・区間最大値・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mx,mn,l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.mn=f;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最大値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.sq=mint(f)*f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mn=f;
    x.sq=mint(f)*f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最大値・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.mn=f;
    x.sq=mint(f)*f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間和・区間最大値・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long l,r,g,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    x.sum=f*x.len;
    x.mx=f;
    x.mn=f;
    x.sq=mint(f)*f*x.len;
    x.l=f;
    x.r=f;
    x.g=0;
    return x;
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間最小値と個数・区間最大値と個数

```cpp
const long long INF=1e18;
struct S{long long mn,mncnt,mx,mxcnt,len;};
using F=long long;
const F ID=LLONG_MIN;
S op(S x,S y){
    S r; r.len=x.len+y.len;
    if(x.mn<y.mn) r.mn=x.mn,r.mncnt=x.mncnt;
    else if(x.mn>y.mn) r.mn=y.mn,r.mncnt=y.mncnt;
    else r.mn=x.mn,r.mncnt=x.mncnt+y.mncnt;
    if(x.mx>y.mx) r.mx=x.mx,r.mxcnt=x.mxcnt;
    else if(x.mx<y.mx) r.mx=y.mx,r.mxcnt=y.mxcnt;
    else r.mx=x.mx,r.mxcnt=x.mxcnt+y.mxcnt;
    return r;
}
S e(){return {INF,0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f==ID) return x;
    return S{f,x.len,f,x.len,x.len};
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, 1, a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (個数 p.mncnt), 最大値 = p.mx (個数 p.mxcnt)
```

## 区間和・区間 XOR 和

```cpp
struct S{long long sum,x,len;};
using F=long long;
const F ID=-1;  // 代入する値は非負
S op(S a,S b){return {a.sum+b.sum,a.x^b.x,a.len+b.len};}
S e(){return {0,0,0};}
S mapping(F f,S x){return f==ID?x:S{f*x.len,(x.len&1)?f:0,x.len};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, XOR = p.x
```

## ローリングハッシュ（回文判定つき）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const mint B=1000003;
struct S{mint h,rh,pw,geo;};  // pw = B^len, geo = 1+B+...+B^(len-1)
using F=long long;
const F ID=-1;
S op(S a,S b){
    return {a.h*b.pw+b.h, b.rh*a.pw+a.rh, a.pw*b.pw, a.geo*b.pw+b.geo};
}
S e(){return {0,0,1,0};}
S mapping(F f,S x){
    if(f==ID) return x;
    mint v=mint(f)*x.geo;
    return {v,v,x.pw,x.geo};
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {c_i, c_i, B, 1}
// 取得: auto p=seg.prod(l,r); ハッシュ = p.h, 回文 <=> p.h==p.rh
// B=10 にすると h は数字列を 10 進数として読んだ値 (mod)
```

## 区間の関数合成（一次関数の代入 + 区間合成）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint a,b; long long len;};  // x -> a x + b,  左から順に適用
struct F{bool upd; mint a,b;};
S op(S l,S r){return {r.a*l.a,r.a*l.b+r.b,l.len+r.len};}
S e(){return {1,0,0};}
S mapping(F f,S x){
    if(!f.upd) return x;
    S r=e(),p{f.a,f.b,1};
    for(long long n=x.len;n;n>>=1,p=op(p,p)) if(n&1) r=op(r,p);
    return r;
}
F composition(F f,F g){return f.upd?f:g;}
F id(){return {false,0,0};}
// 初期値: {a_i, b_i, 1}
// 取得: auto p=seg.prod(l,r); 合成した関数 x -> p.a*x + p.b
// 巨大な配列: 座標圧縮して 1 要素を長さ len の区間にし、初期値の関数を len 回合成したものにする
```

## 区間の行列積（行列の代入 + 区間積）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=2;
using M=std::array<std::array<mint,K>,K>;
M mul(const M&a,const M&b){
    M r{};
    for(int i=0;i<K;i++) for(int k=0;k<K;k++) for(int j=0;j<K;j++) r[i][j]+=a[i][k]*b[k][j];
    return r;
}
M unit(){M r{}; for(int i=0;i<K;i++) r[i][i]=1; return r;}
struct S{M m; long long len;};
struct F{bool upd; M m;};
S op(S a,S b){return {mul(a.m,b.m),a.len+b.len};}
S e(){return {unit(),0};}
S mapping(F f,S x){
    if(!f.upd) return x;
    M r=unit(),p=f.m;
    for(long long n=x.len;n;n>>=1,p=mul(p,p)) if(n&1) r=mul(r,p);
    return {r,x.len};
}
F composition(F f,F g){return f.upd?f:g;}
F id(){return {false,unit()};}
// 初期値: {M_i, 1}
// 取得: auto p=seg.prod(l,r); 行列積 = p.m
// prod(l,r).m = M_l M_{l+1} ... M_{r-1}
// 部分列 "abc" の個数など: 文字ごとの遷移行列を並べる
```

## 区間に現れる値の集合（値域が 64 以下）

```cpp
using S=unsigned long long;  // 現れる値の集合
using F=int;  // 代入する値 (0..63)
const F ID=-1;
S op(S a,S b){return a|b;}
S e(){return 0;}
S mapping(F f,S x){return (f==ID||x==0)?x:1ULL<<f;}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: 1ULL<<a_i
// 取得: 集合 = seg.prod(l,r), 種類数 = std::popcount(集合), mex = std::countr_one(集合)
```

## 区間和・最大値・最小値・二乗和・GCD・XOR・積・OR・AND

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long l,r,g,x; mint prod; long long orv,andv,len;};
using F=long long;
const F ID=LLONG_MIN;  // XOR・OR・AND を使うときは代入する値は非負
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,
            a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),
            a.x^b.x,a.prod*b.prod,a.orv|b.orv,a.andv&b.andv,a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0,0,1,0,-1,0};}
S mapping(F f,S x){
    if(f==ID||x.len==0) return x;
    return {f*x.len,f,f,mint(f)*f*x.len,f,f,0,(x.len&1)?f:0,mint(f).pow(x.len),f,f,x.len};
}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, a_i, a_i, a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g), XOR = p.x, 積 = p.prod, OR = p.orv, AND = p.andv
```

## 区間 LCM

```cpp
using S=long long;
using F=long long;
const F ID=-1;  // 代入する値は 1 以上
S op(S a,S b){return std::lcm(a,b);}
S e(){return 1;}
S mapping(F f,S x){return f==ID?x:f;}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 取得: LCM = seg.prod(l,r)  (オーバーフローに注意)
```

## 区間 GCD・LCM

```cpp
struct S{long long g,lc;};
using F=long long;
const F ID=-1;  // 代入する値は 1 以上
S op(S a,S b){return {std::gcd(a.g,b.g),std::lcm(a.lc,b.lc)};}
S e(){return {0,1};}
S mapping(F f,S x){return f==ID?x:S{f,f};}
F composition(F f,F g){return f==ID?g:f;}
F id(){return ID;}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); GCD = p.g, LCM = p.lc  (オーバーフローに注意)
```

## 両方向の関数合成（一次関数の代入 + 左から・右からの合成, HLD 用）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

struct S{mint a,b,ra,rb; long long len;};  // (a,b): 左から順に適用, (ra,rb): 右から順に適用
struct F{bool upd; mint a,b;};
S op(S l,S r){return {r.a*l.a,r.a*l.b+r.b,l.ra*r.ra,l.ra*r.rb+l.rb,l.len+r.len};}
S e(){return {1,0,1,0,0};}
S mapping(F f,S x){
    if(!f.upd) return x;
    S r=e(),p{f.a,f.b,f.a,f.b,1};
    for(long long n=x.len;n;n>>=1,p=op(p,p)) if(n&1) r=op(r,p);
    return r;
}
F composition(F f,F g){return f.upd?f:g;}
F id(){return {false,0,0};}
// 初期値: {a_i, b_i, a_i, b_i, 1}
// 取得: auto p=seg.prod(l,r); 左から: x -> p.a*x + p.b, 右から: x -> p.ra*x + p.rb
```

## 任意のモノイドの代入 + 区間積（例: クランプ関数の合成）

```cpp
// T: 任意のモノイド (tmul: 結合的な演算, tunit: 単位元)。例として x -> min(max(x+add, lo), hi) の合成
// 他の例: 行列 (行列積), max-plus 行列 (DP の遷移), 一次関数, 文字列ハッシュ (h, B^len)
const long long INF=1e18;
struct T{long long add,lo,hi;};
long long clamp_(long long x,long long lo,long long hi){return std::min(std::max(x,lo),hi);}
T tmul(T f,T g){return {f.add+g.add,clamp_(f.lo+g.add,g.lo,g.hi),clamp_(f.hi+g.add,g.lo,g.hi)};}  // f の後に g
T tunit(){return {0,-INF,INF};}
struct S{T v; long long len;};
struct F{bool upd; T v;};
S op(S a,S b){return {tmul(a.v,b.v),a.len+b.len};}
S e(){return {tunit(),0};}
S mapping(F f,S x){
    if(!f.upd) return x;
    T r=tunit(),p=f.v;
    for(long long n=x.len;n;n>>=1,p=tmul(p,p)) if(n&1) r=tmul(r,p);
    return {r,x.len};
}
F composition(F f,F g){return f.upd?f:g;}
F id(){return {false,tunit()};}
// 初期値: {T_i, 1}
// 取得: auto p=seg.prod(l,r); 積 = p.v  (例: x に左から順に適用した結果 = clamp_(x+p.v.add, p.v.lo, p.v.hi))
```

# 3. 区間加算 + 区間更新

## 区間和

```cpp
struct S{long long sum; long long len;};
struct F{bool upd; long long v;};
S op(S a,S b){return {a.sum+b.sum,a.len+b.len};}
S e(){return {0,0};}
S mapping(F f,S x){return {f.upd?f.v*x.len:x.sum+f.v*x.len,x.len};}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値

```cpp
const long long INF=1e18;
using S=long long;
struct F{bool upd; long long v;};
S op(S a,S b){return std::max(a,b);}
S e(){return -INF;}
S mapping(F f,S x){return f.upd?f.v:x+f.v;}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 加算: {false,v}, 代入: {true,v}
// 取得: 最大値 = seg.prod(l,r)
```

## 区間最小値

```cpp
const long long INF=1e18;
using S=long long;
struct F{bool upd; long long v;};
S op(S a,S b){return std::min(a,b);}
S e(){return INF;}
S mapping(F f,S x){return f.upd?f.v:x+f.v;}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 加算: {false,v}, 代入: {true,v}
// 取得: 最小値 = seg.prod(l,r)
```

## 区間最大値とその個数

```cpp
const long long INF=1e18;
struct S{long long mx,cnt,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.mx>b.mx) return {a.mx,a.cnt,a.len+b.len};
    if(a.mx<b.mx) return {b.mx,b.cnt,a.len+b.len};
    return {a.mx,a.cnt+b.cnt,a.len+b.len};
}
S e(){return {-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    return f.upd?S{f.v,x.len,x.len}:S{x.mx+f.v,x.cnt,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 個数 = p.cnt
// 加算: {false,v}, 代入: {true,v}
```

## 区間最小値とその個数

```cpp
const long long INF=1e18;
struct S{long long mn,cnt,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.mn<b.mn) return {a.mn,a.cnt,a.len+b.len};
    if(a.mn>b.mn) return {b.mn,b.cnt,a.len+b.len};
    return {a.mn,a.cnt+b.cnt,a.len+b.len};
}
S e(){return {INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    return f.upd?S{f.v,x.len,x.len}:S{x.mn+f.v,x.cnt,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 個数 = p.cnt
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値とその位置

```cpp
const long long INF=1e18;
struct S{long long mx; int idx; int l;};  // 最大値, その最左位置, 区間の左端
struct F{bool upd; long long v;};
S op(S a,S b){
    S r=a.mx>=b.mx?a:b;
    r.l=std::min(a.l,b.l);
    return r;
}
S e(){return {-INF,INT_MAX,INT_MAX};}
S mapping(F f,S x){
    if(x.l==INT_MAX) return x;
    return f.upd?S{f.v,x.l,x.l}:S{x.mx+f.v,x.idx,x.l};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, i, i}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最左位置 = p.idx
// 加算: {false,v}, 代入: {true,v}
```

## 区間最小値とその位置

```cpp
const long long INF=1e18;
struct S{long long mn; int idx; int l;};  // 最小値, その最左位置, 区間の左端
struct F{bool upd; long long v;};
S op(S a,S b){
    S r=a.mn<=b.mn?a:b;
    r.l=std::min(a.l,b.l);
    return r;
}
S e(){return {INF,INT_MAX,INT_MAX};}
S mapping(F f,S x){
    if(x.l==INT_MAX) return x;
    return f.upd?S{f.v,x.l,x.l}:S{x.mn+f.v,x.idx,x.l};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, i, i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最左位置 = p.idx
// 加算: {false,v}, 代入: {true,v}
```

## 区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint sum; mint sq; mint len;};
struct F{bool upd; mint v;};
S op(S a,S b){return {a.sum+b.sum,a.sq+b.sq,a.len+b.len};}
S e(){return {0,0,0};}
S mapping(F f,S x){
    if(f.upd) return {f.v*x.len,f.v*f.v*x.len,x.len};
    return {x.sum+f.v*x.len,x.sq+2*f.v*x.sum+f.v*f.v*x.len,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 二乗和 = p.sq, 和 = p.sum
// 加算: {false,v}, 代入: {true,v}
```

## 区間 GCD

```cpp
struct S{long long l,r,g,len;};  // 左端の値, 右端の値, 隣接差の GCD
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {f.v,f.v,0,x.len};
    return {x.l+f.v,x.r+f.v,x.g,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); GCD = std::gcd(std::abs(p.l), p.g), 全部等しい <=> p.g==0
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最大値

```cpp
const long long INF=1e18;
struct S{long long sum,mx,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.len+b.len};
}
S e(){return {0,-INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
    }else{
        x.sum+=f.v*x.len;
        x.mx+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最小値

```cpp
const long long INF=1e18;
struct S{long long sum,mn,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {0,INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mn=f.v;
    }else{
        x.sum+=f.v*x.len;
        x.mn+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.len+b.len};
}
S e(){return {0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.sq=mint(f.v)*f.v*x.len;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 二乗和 = p.sq
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間 GCD

```cpp
struct S{long long sum,l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sum+=f.v*x.len;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・区間最小値

```cpp
const long long INF=1e18;
struct S{long long mx,mn,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {-INF,INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.mx=f.v;
        x.mn=f.v;
    }else{
        x.mx+=f.v;
        x.mn+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.sq=mint(f.v)*f.v*x.len;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mx+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 二乗和 = p.sq
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mx,l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {-INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.mx=f.v;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.mx+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mn=f.v;
        x.sq=mint(f.v)*f.v*x.len;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mn+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 二乗和 = p.sq
// 加算: {false,v}, 代入: {true,v}
```

## 区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mn,l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.mn=f.v;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.mn+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.sq=mint(f.v)*f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最大値・区間最小値

```cpp
const long long INF=1e18;
struct S{long long sum,mx,mn,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.len+b.len};
}
S e(){return {0,-INF,INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.mn=f.v;
    }else{
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.mn+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最大値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.sq=mint(f.v)*f.v*x.len;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mx+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 二乗和 = p.sq
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最大値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mx,l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mn=f.v;
        x.sq=mint(f.v)*f.v*x.len;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mn+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 二乗和 = p.sq
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mn,l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mn=f.v;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sum+=f.v*x.len;
        x.mn+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{long long sum; mint sq; long long l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.sq=mint(f.v)*f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.mn=f.v;
        x.sq=mint(f.v)*f.v*x.len;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.mn+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long mx,mn,l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {-INF,INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.mx=f.v;
        x.mn=f.v;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.mx+=f.v;
        x.mn+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.sq=mint(f.v)*f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mn=f.v;
        x.sq=mint(f.v)*f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mn+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最大値・区間最小値・区間二乗和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.len+b.len};
}
S e(){return {0,-INF,INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.mn=f.v;
        x.sq=mint(f.v)*f.v*x.len;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.mn+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最大値・区間最小値・区間 GCD

```cpp
const long long INF=1e18;
struct S{long long sum,mx,mn,l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.mn=f.v;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.mn+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最大値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx; mint sq; long long l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.sq=mint(f.v)*f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mn; mint sq; long long l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mn=f.v;
        x.sq=mint(f.v)*f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mn+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.mn=f.v;
        x.sq=mint(f.v)*f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.mn+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間和・区間最大値・区間最小値・区間二乗和・区間 GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const long long INF=1e18;
struct S{long long sum,mx,mn; mint sq; long long l,r,g,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.sq+b.sq,a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,-INF,INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd){
        x.sum=f.v*x.len;
        x.mx=f.v;
        x.mn=f.v;
        x.sq=mint(f.v)*f.v*x.len;
        x.l=f.v;
        x.r=f.v;
        x.g=0;
    }else{
        x.sq+=2*mint(f.v)*x.sum+mint(f.v)*f.v*x.len;
        x.sum+=f.v*x.len;
        x.mx+=f.v;
        x.mn+=f.v;
        x.l+=f.v;
        x.r+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算: {false,v}, 代入: {true,v}
```

## 区間最小値と個数・区間最大値と個数

```cpp
const long long INF=1e18;
struct S{long long mn,mncnt,mx,mxcnt,len;};
struct F{bool upd; long long v;};
S op(S x,S y){
    S r; r.len=x.len+y.len;
    if(x.mn<y.mn) r.mn=x.mn,r.mncnt=x.mncnt;
    else if(x.mn>y.mn) r.mn=y.mn,r.mncnt=y.mncnt;
    else r.mn=x.mn,r.mncnt=x.mncnt+y.mncnt;
    if(x.mx>y.mx) r.mx=x.mx,r.mxcnt=x.mxcnt;
    else if(x.mx<y.mx) r.mx=y.mx,r.mxcnt=y.mxcnt;
    else r.mx=x.mx,r.mxcnt=x.mxcnt+y.mxcnt;
    return r;
}
S e(){return {INF,0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return S{f.v,x.len,f.v,x.len,x.len};
    return S{x.mn+f.v,x.mncnt,x.mx+f.v,x.mxcnt,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, 1, a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (個数 p.mncnt), 最大値 = p.mx (個数 p.mxcnt)
// 加算: {false,v}, 代入: {true,v}
```

## 隣接要素の大小（上昇・下降の個数 / ソート済み判定）

```cpp
struct S{long long l,r,up,down,len;};  // up: x_i<x_{i+1} の個数, down: x_i>x_{i+1} の個数
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.l,b.r,a.up+b.up+(a.r<b.l),a.down+b.down+(a.r>b.l),a.len+b.len};
}
S e(){return {0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {f.v,f.v,0,0,x.len};
    return {x.l+f.v,x.r+f.v,x.up,x.down,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 0, 0, 1}
// 取得: auto p=seg.prod(l,r); 上昇 = p.up, 下降 = p.down, 広義単調増加 <=> p.down==0
// 広義単調増加 <=> down==0,  同じ値の箇所 = len-1-up-down
// 加算: {false,v}, 代入: {true,v}
```

## 連続する同じ値のまとまりの個数（ランの数）

```cpp
struct S{long long l; long long r; long long cnt;};  // 左端の値, 右端の値, ランの数
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.cnt==0) return b;
    if(b.cnt==0) return a;
    return {a.l,b.r,a.cnt+b.cnt-(a.r==b.l)};
}
S e(){return {0,0,0};}
S mapping(F f,S x){
    if(x.cnt==0) return x;
    if(f.upd) return {f.v,f.v,1};
    return {x.l+f.v,x.r+f.v,x.cnt};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); ランの数 = p.cnt
// x_i!=x_{i+1} の個数 = cnt-1
// 加算: {false,v}, 代入: {true,v}
```

## 同じ値が連続する最長の長さ

```cpp
struct S{long long len,lv,rv,pre,suf,best;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    bool c=a.rv==b.lv;
    return {a.len+b.len,a.lv,b.rv,
            (c&&a.pre==a.len)?a.len+b.pre:a.pre,
            (c&&b.suf==b.len)?b.len+a.suf:b.suf,
            std::max({a.best,b.best,c?a.suf+b.pre:0})};
}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {x.len,f.v,f.v,x.len,x.len,x.len};
    return {x.len,x.lv+f.v,x.rv+f.v,x.pre,x.suf,x.best};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {1, a_i, a_i, 1, 1, 1}
// 取得: auto p=seg.prod(l,r); 最長 = p.best
// 加算: {false,v}, 代入: {true,v}
```

## 最長の狭義単調増加な連続部分列の長さ

```cpp
struct S{long long len,lv,rv,pre,suf,best;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    bool c=a.rv<b.lv;
    return {a.len+b.len,a.lv,b.rv,
            (c&&a.pre==a.len)?a.len+b.pre:a.pre,
            (c&&b.suf==b.len)?b.len+a.suf:b.suf,
            std::max({a.best,b.best,c?a.suf+b.pre:0})};
}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {x.len,f.v,f.v,1,1,1};
    return {x.len,x.lv+f.v,x.rv+f.v,x.pre,x.suf,x.best};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {1, a_i, a_i, 1, 1, 1}
// 取得: auto p=seg.prod(l,r); 最長 = p.best
// 広義なら <=、減少なら > / >=
// 加算: {false,v}, 代入: {true,v}
```

## max_{i<=j} (x_j - x_i)

```cpp
const long long INF=1e18;
struct S{long long mn,mx,best;};
struct F{bool upd; long long v;};
S op(S a,S b){return {std::min(a.mn,b.mn),std::max(a.mx,b.mx),std::max({a.best,b.best,b.mx-a.mn})};}
S e(){return {INF,-INF,-INF};}
S mapping(F f,S x){
    if(x.mn>x.mx) return x;
    if(f.upd) return {f.v,f.v,0};
    return {x.mn+f.v,x.mx+f.v,x.best};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 0}
// max_{i<=j}(x_i - x_j) は a.mx-b.mn にする
// 初期値を a_i - i にすると max_{i<=j} (x_j - x_i) - (j - i)
// 取得: auto p=seg.prod(l,r); max (x_j - x_i) = p.best
// min_{i<=j} (x_j - x_i) は符号を反転して持つ
// 加算: {false,v}, 代入: {true,v}
```

## 異なる 2 要素の和の最大 max_{i<j} (x_i + x_j)

```cpp
const long long INF=1e18;
struct S{long long mx,best,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    long long c=(a.len&&b.len)?a.mx+b.mx:-INF;
    return {std::max(a.mx,b.mx),std::max({a.best,b.best,c}),a.len+b.len};
}
S e(){return {-INF,-INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {f.v,x.len>=2?2*f.v:-INF,x.len};
    return {x.mx+f.v,x.best==-INF?-INF:x.best+2*f.v,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, -INF, 1}
// 取得: auto p=seg.prod(l,r); max (x_i + x_j) = p.best (要素が 1 個なら -INF)
// 加算: {false,v}, 代入: {true,v}
```

## 隣接差の絶対値の和 Σ|x_{i+1} - x_i|

```cpp
struct S{long long l,r,d,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.l,b.r,a.d+b.d+std::abs(a.r-b.l),a.len+b.len};  // 上昇量の和なら std::max(0LL,b.l-a.r)
}
S e(){return {0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {f.v,f.v,0,x.len};
    return {x.l+f.v,x.r+f.v,x.d,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); Σ|x_{i+1} - x_i| = p.d
// 加算: {false,v}, 代入: {true,v}
```

## 隣接差の絶対値の最大 max|x_{i+1} - x_i|

```cpp
struct S{long long l,r,d,len;};
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.l,b.r,std::max({a.d,b.d,std::abs(a.r-b.l)}),a.len+b.len};
}
S e(){return {0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {f.v,f.v,0,x.len};
    return {x.l+f.v,x.r+f.v,x.d,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); max|x_{i+1} - x_i| = p.d
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・2 番目の最大値とその個数

```cpp
const long long INF=1e18;
struct S{long long m1,c1,m2,c2,len;};  // 最大値, 個数, 2 番目に大きい値 (なければ -INF), 個数
struct F{bool upd; long long v;};
S op(S a,S b){
    long long v[4]={a.m1,a.m2,b.m1,b.m2},c[4]={a.c1,a.c2,b.c1,b.c2};
    S r{-INF,0,-INF,0,a.len+b.len};
    for(int i=0;i<4;i++){
        if(v[i]==-INF) continue;
        if(v[i]>r.m1){r.m2=r.m1; r.c2=r.c1; r.m1=v[i]; r.c1=c[i];}
        else if(v[i]==r.m1) r.c1+=c[i];
        else if(v[i]>r.m2){r.m2=v[i]; r.c2=c[i];}
        else if(v[i]==r.m2) r.c2+=c[i];
    }
    return r;
}
S e(){return {-INF,0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {f.v,x.len,-INF,0,x.len};
    return {x.m1+f.v,x.c1,x.m2==-INF?-INF:x.m2+f.v,x.c2,x.len};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, 1, -INF, 0, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.m1 (個数 p.c1), 2 番目 = p.m2 (個数 p.c2)
// 加算: {false,v}, 代入: {true,v}
```

## 固定オフセット付き最小値 min(x_i + c_i)

```cpp
const long long INF=1e18;
struct S{long long m,cmin;};  // min(x_i + c_i), min c_i
struct F{bool upd; long long v;};
S op(S a,S b){return {std::min(a.m,b.m),std::min(a.cmin,b.cmin)};}
S e(){return {INF,INF};}
S mapping(F f,S x){
    if(x.cmin==INF) return x;
    return {f.upd?f.v+x.cmin:x.m+f.v,x.cmin};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i + c_i, c_i}
// 取得: auto p=seg.prod(l,r); min (x_i + c_i) = p.m
// 最大値版は min/max, INF/-INF を入れ替える
// 加算: {false,v}, 代入: {true,v}
```

## 上位 K 個の値（重複込み）

```cpp
const long long INF=1e18;
const int K=3;
struct S{long long v[K]; long long len;};  // 大きい順に K 個 (足りない分は -INF)
struct F{bool upd; long long v;};
S op(S a,S b){
    S r; r.len=a.len+b.len;
    int i=0,j=0;
    for(int k=0;k<K;k++) r.v[k]=(a.v[i]>=b.v[j])?a.v[i++]:b.v[j++];
    return r;
}
S e(){S r; for(int k=0;k<K;k++) r.v[k]=-INF; r.len=0; return r;}
S mapping(F f,S x){
    for(int k=0;k<K;k++){
        if(f.upd) x.v[k]=k<x.len?f.v:-INF;
        else if(x.v[k]!=-INF) x.v[k]+=f.v;
    }
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: v = {a_i, -INF, ...}, len = 1
// 取得: auto p=seg.prod(l,r); k 番目 (0-indexed) に大きい値 = p.v[k]
// 下位 K 個は符号を反転して持つ
// 異なる 2 要素の積の最大 = max(上位 2 個の積, 下位 2 個の積)
// 加算: {false,v}, 代入: {true,v}
```

## 歴史的最大値

```cpp
const long long INF=1e18;
struct S{long long mx,hmx;};  // 現在の最大値, 歴史的最大値
struct F{bool upd; long long v,p,q;};
// upd=false: x += v,  歴史に x+p (p: 途中の加算量の最大)
// upd=true : x = v,   歴史に x+p (代入前の途中の最大) と q (代入後に取った値の最大)
S op(S a,S b){return {std::max(a.mx,b.mx),std::max(a.hmx,b.hmx)};}
S e(){return {-INF,-INF};}
S mapping(F f,S x){
    if(x.mx==-INF) return x;
    if(!f.upd) return {x.mx+f.v,std::max(x.hmx,x.mx+f.p)};
    return {f.v,std::max({x.hmx,x.mx+f.p,f.q})};
}
F composition(F f,F g){
    if(!g.upd&&!f.upd) return {false,g.v+f.v,std::max(g.p,g.v+f.p),-INF};
    if(!g.upd) return {true,f.v,std::max(g.p,g.v+f.p),f.q};
    if(!f.upd) return {true,g.v+f.v,g.p,std::max(g.q,g.v+f.p)};
    return {true,f.v,g.p,std::max({g.q,g.v+f.p,f.q})};
}
F id(){return {false,0,0,-INF};}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 歴史的最大値 = p.hmx, 現在の最大値 = p.mx
// 加算 v: {false,v,max(v,0),-INF}, 代入 v: {true,v,0,v}
```

## 歴史的最小値

```cpp
const long long INF=1e18;
struct S{long long mn,hmn;};  // 現在の最小値, 歴史的最小値
struct F{bool upd; long long v,p,q;};
// upd=false: x += v,  歴史に x+p (p: 途中の加算量の最小)
// upd=true : x = v,   歴史に x+p (代入前の途中の最小) と q (代入後に取った値の最小)
S op(S a,S b){return {std::min(a.mn,b.mn),std::min(a.hmn,b.hmn)};}
S e(){return {INF,INF};}
S mapping(F f,S x){
    if(x.mn==INF) return x;
    if(!f.upd) return {x.mn+f.v,std::min(x.hmn,x.mn+f.p)};
    return {f.v,std::min({x.hmn,x.mn+f.p,f.q})};
}
F composition(F f,F g){
    if(!g.upd&&!f.upd) return {false,g.v+f.v,std::min(g.p,g.v+f.p),INF};
    if(!g.upd) return {true,f.v,std::min(g.p,g.v+f.p),f.q};
    if(!f.upd) return {true,g.v+f.v,g.p,std::min(g.q,g.v+f.p)};
    return {true,f.v,g.p,std::min({g.q,g.v+f.p,f.q})};
}
F id(){return {false,0,0,INF};}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 歴史的最小値 = p.hmn, 現在の最小値 = p.mn
// 加算 v: {false,v,min(v,0),INF}, 代入 v: {true,v,0,v}
```

## 値を M で割った余りごとの個数・区間和

```cpp
const int M=2;
struct S{long long cnt[M]; long long sum;};  // cnt[r]: x_i ≡ r (mod M) の個数
struct F{bool upd; long long v;};
S op(S a,S b){for(int r=0;r<M;r++) a.cnt[r]+=b.cnt[r]; a.sum+=b.sum; return a;}
S e(){return S{};}
S mapping(F f,S x){
    long long len=0; for(int r=0;r<M;r++) len+=x.cnt[r];
    S y{};
    if(f.upd){y.cnt[(f.v%M+M)%M]=len; y.sum=f.v*len; return y;}
    for(int r=0;r<M;r++) y.cnt[((r+f.v)%M+M)%M]=x.cnt[r];
    y.sum=x.sum+f.v*len;
    return y;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: cnt[a_i mod M]=1, sum=a_i
// 取得: auto p=seg.prod(l,r); x_i ≡ r (mod M) の個数 = p.cnt[r], 和 = p.sum, Σ (x_i mod M) = Σ r*p.cnt[r]
// 加算: {false,v}, 代入: {true,v}
```

## 全ての連続部分列の和の総和

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

struct S{mint s[3],w[3];};  // s[k] = Σ i^k x_i, w[k] = Σ i^k
struct F{bool upd; mint v;};
S op(S a,S b){for(int k=0;k<3;k++){a.s[k]+=b.s[k]; a.w[k]+=b.w[k];} return a;}
S e(){return S{};}
S mapping(F f,S x){
    for(int k=0;k<3;k++) x.s[k]=(f.upd?0:x.s[k])+f.v*x.w[k];
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: s = {a_i, i*a_i, i*i*a_i}, w = {1, i, i*i}
// 取得: auto p=seg.prod(l,r); 総和 Σ_{l<=a<=b<r} (x_a+...+x_b) = -p.s[2] + mint(r+l-1)*p.s[1] + mint(r)*(1-l)*p.s[0]
// 加算: {false,v}, 代入: {true,v}
```

## 区間最大値・最小値とその個数・位置

```cpp
const long long INF=1e18;
struct S{long long mx,mxcnt,mn,mncnt; int imx,imn,lft; long long len;};  // imx, imn: 最左位置, lft: 区間の左端
struct F{bool upd; long long v;};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    S r=a; r.len=a.len+b.len;
    if(b.mx>a.mx) r.mx=b.mx,r.mxcnt=b.mxcnt,r.imx=b.imx;
    else if(b.mx==a.mx) r.mxcnt+=b.mxcnt;
    if(b.mn<a.mn) r.mn=b.mn,r.mncnt=b.mncnt,r.imn=b.imn;
    else if(b.mn==a.mn) r.mncnt+=b.mncnt;
    return r;
}
S e(){return {-INF,0,INF,0,-1,-1,-1,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {f.v,x.len,f.v,x.len,x.lft,x.lft,x.lft,x.len};
    x.mx+=f.v; x.mn+=f.v;
    return x;
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.v+f.v};}
F id(){return {false,0};}
// 初期値: {a_i, 1, a_i, 1, i, i, i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx (個数 p.mxcnt, 最左位置 p.imx), 最小値 = p.mn (個数 p.mncnt, 最左位置 p.imn)
// 加算: {false,v}, 代入: {true,v}
```

# 4. 区間乗算・区間アフィン変換 (x ← ax + b)

## 区間乗算 + 区間和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
using S=mint;
using F=mint;
S op(S a,S b){return a+b;}
S e(){return 0;}
S mapping(F f,S x){return f*x;}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 取得: 和 = seg.prod(l,r)
```

## 区間乗算 + 区間 k 乗和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=3;
struct S{mint p[K+1];};  // p[j] = Σ x_i^j
using F=mint;
S op(S a,S b){for(int j=0;j<=K;j++) a.p[j]+=b.p[j]; return a;}
S e(){return S{};}
S mapping(F f,S x){
    mint v=1;
    for(int j=0;j<=K;j++){x.p[j]*=v; v*=f;}
    return x;
}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: p[j] = a_i^j
// 取得: auto p=seg.prod(l,r); Σ x_i^k = p.p[k]
```

## 区間乗算 + 区間積 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint prod; long long len;};
using F=mint;
S op(S a,S b){return {a.prod*b.prod,a.len+b.len};}
S e(){return {1,0};}
S mapping(F f,S x){return {x.prod*f.pow(x.len),x.len};}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 積 = p.prod
```

## 区間乗算 + 区間積・素因数の集合（積のオイラー関数）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

struct S{mint prod; unsigned long long mask; long long len;};  // mask: 現れる素因数の集合
struct F{mint mul; unsigned long long mask;};
S op(S a,S b){return {a.prod*b.prod,a.mask|b.mask,a.len+b.len};}
S e(){return {1,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    return {x.prod*f.mul.pow(x.len),x.mask|f.mask,x.len};
}
F composition(F f,F g){return {f.mul*g.mul,f.mask|g.mask};}
F id(){return {1,0};}
// 初期値: {a_i, a_i の素因数の集合, 1}  (素数は 64 個まで)
// 取得: auto p=seg.prod(l,r); 積 = p.prod, 素因数の集合 = p.mask
// φ(積) = prod * Π_{p∈mask} (p-1)/p
```

## 区間乗算 + 区間 GCD

```cpp
using S=long long;
using F=long long;
S op(S a,S b){return std::gcd(a,b);}
S e(){return 0;}
S mapping(F f,S x){return std::abs(f)*x;}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: |a_i|
// 取得: GCD = seg.prod(l,r)
```

## 区間乗算 + 区間最大部分和・最小部分和

```cpp
const long long INF=1e18;
struct S{long long sum,premx,premn,sufmx,sufmn,bestmx,bestmn,len;};
using F=long long;
S op(S a,S b){
    return {a.sum+b.sum,
            std::max(a.premx,a.sum+b.premx),
            std::min(a.premn,a.sum+b.premn),
            std::max(b.sufmx,b.sum+a.sufmx),
            std::min(b.sufmn,b.sum+a.sufmn),
            std::max({a.bestmx,b.bestmx,a.sufmx+b.premx}),
            std::min({a.bestmn,b.bestmn,a.sufmn+b.premn}),
            a.len+b.len};
}
S e(){return {0,-INF,INF,-INF,INF,-INF,INF,0};}
S mapping(F f,S x){
    if(x.len==0||f==1) return x;
    if(f==0) return {0,0,0,0,0,0,0,x.len};
    if(f>0) return {f*x.sum,f*x.premx,f*x.premn,f*x.sufmx,f*x.sufmn,f*x.bestmx,f*x.bestmn,x.len};
    return {f*x.sum,f*x.premn,f*x.premx,f*x.sufmn,f*x.sufmx,f*x.bestmn,f*x.bestmx,x.len};
}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: {a_i, a_i, a_i, a_i, a_i, a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 最大部分和 = p.bestmx, 最小部分和 = p.bestmn
```

## 区間乗算 + 区間最小値・最大値（負の数もかけられる）

```cpp
const long long INF=1e18;
struct S{long long mn,mx;};
using F=long long;
S op(S a,S b){return {std::min(a.mn,b.mn),std::max(a.mx,b.mx)};}
S e(){return {INF,-INF};}
S mapping(F f,S x){
    if(x.mn>x.mx) return x;
    return f>=0?S{f*x.mn,f*x.mx}:S{f*x.mx,f*x.mn};
}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最大値 = p.mx
```

## 区間乗算 + 区間和・最小値・最大値

```cpp
const long long INF=1e18;
struct S{long long sum,mn,mx;};
using F=long long;
S op(S a,S b){return {a.sum+b.sum,std::min(a.mn,b.mn),std::max(a.mx,b.mx)};}
S e(){return {0,INF,-INF};}
S mapping(F f,S x){
    if(x.mn>x.mx) return x;
    return f>=0?S{f*x.sum,f*x.mn,f*x.mx}:S{f*x.sum,f*x.mx,f*x.mn};
}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: {a_i, a_i, a_i}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 最大値 = p.mx
```

## 区間アフィン + 区間和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint sum; mint len;};
struct F{mint a; mint b;};
S op(S x,S y){return {x.sum+y.sum,x.len+y.len};}
S e(){return {0,0};}
S mapping(F f,S x){return {f.a*x.sum+f.b*x.len,x.len};}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 点の値 = seg.get(i).sum
// 加算 v: {1,v}, 乗算 v: {v,0}, 代入 v: {0,v}
// 巨大な配列: 座標圧縮して 1 要素を長さ len の区間 [X_k, X_{k+1}) にする (初期値 {0, X_{k+1}-X_k})
```

## 区間アフィン + 区間二乗和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint sum; mint sq; mint len;};
struct F{mint a; mint b;};
S op(S x,S y){return {x.sum+y.sum,x.sq+y.sq,x.len+y.len};}
S e(){return {0,0,0};}
S mapping(F f,S x){
    return {f.a*x.sum+f.b*x.len,
            f.a*f.a*x.sq+2*f.a*f.b*x.sum+f.b*f.b*x.len,
            x.len};
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, a_i*a_i, 1}
// 取得: auto p=seg.prod(l,r); 二乗和 = p.sq, 和 = p.sum
```

## 区間アフィン + 区間 k 乗和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=3;
struct S{mint p[K+1];};  // p[j] = Σ x_i^j  (p[0] = 長さ)
struct F{mint a,b;};
S op(S x,S y){for(int j=0;j<=K;j++) x.p[j]+=y.p[j]; return x;}
S e(){return S{};}
S mapping(F f,S x){
    static mint C[K+1][K+1];
    if(C[0][0]==0) for(int i=0;i<=K;i++){C[i][0]=1; for(int j=1;j<=i;j++) C[i][j]=C[i-1][j-1]+C[i-1][j];}
    mint ap[K+1],bp[K+1]; ap[0]=bp[0]=1;
    for(int j=1;j<=K;j++){ap[j]=ap[j-1]*f.a; bp[j]=bp[j-1]*f.b;}
    S r{};
    for(int k=0;k<=K;k++) for(int j=0;j<=k;j++) r.p[k]+=C[k][j]*ap[j]*bp[k-j]*x.p[j];
    return r;
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: p[j] = a_i^j
// 取得: auto p=seg.prod(l,r); Σ x_i^k = p.p[k]
```

## 区間アフィン + 固定重み付き和 Σ w_i x_i (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint wx; mint w;};
struct F{mint a; mint b;};
S op(S x,S y){return {x.wx+y.wx,x.w+y.w};}
S e(){return {0,0};}
S mapping(F f,S x){return {f.a*x.wx+f.b*x.w,x.w};}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {w_i*a_i, w_i}
// 取得: auto p=seg.prod(l,r); Σ w_i x_i = p.wx
```

## 区間アフィン + 区間 GCD

```cpp
struct S{long long l,r,g,len;};  // 左端の値, 右端の値, 隣接差の GCD
struct F{long long a,b;};
S op(S x,S y){
    if(x.len==0) return y;
    if(y.len==0) return x;
    return {x.l,y.r,std::gcd(std::gcd(x.g,y.g),std::abs(y.l-x.r)),x.len+y.len};
}
S e(){return {0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    return {f.a*x.l+f.b,f.a*x.r+f.b,std::abs(f.a)*x.g,x.len};
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); GCD = std::gcd(std::abs(p.l), p.g), 全部等しい <=> p.g==0
```

## 区間アフィン + 区間最小値・最大値（a は負でもよい）

```cpp
const long long INF=1e18;
struct S{long long mn; long long mx;};
struct F{long long a; long long b;};
S op(S x,S y){return {std::min(x.mn,y.mn),std::max(x.mx,y.mx)};}
S e(){return {INF,-INF};}
S mapping(F f,S x){
    if(x.mn>x.mx) return x;
    if(f.a>=0) return {f.a*x.mn+f.b,f.a*x.mx+f.b};
    return {f.a*x.mx+f.b,f.a*x.mn+f.b};
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最大値 = p.mx
```

## 区間アフィン + 区間和・最小値・最大値

```cpp
const long long INF=1e18;
struct S{long long sum,mn,mx,len;};
struct F{long long a,b;};
S op(S x,S y){return {x.sum+y.sum,std::min(x.mn,y.mn),std::max(x.mx,y.mx),x.len+y.len};}
S e(){return {0,INF,-INF,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    long long p=f.a*x.mn+f.b,q=f.a*x.mx+f.b;
    return {f.a*x.sum+f.b*x.len,std::min(p,q),std::max(p,q),x.len};
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, a_i, a_i, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 最大値 = p.mx
```

## 区間アフィン + 区間最小値と個数・最大値と個数

```cpp
const long long INF=1e18;
struct S{long long mn,mncnt,mx,mxcnt,len;};
struct F{long long a; long long b;};
S op(S x,S y){
    S r; r.len=x.len+y.len;
    if(x.mn<y.mn) r.mn=x.mn,r.mncnt=x.mncnt;
    else if(x.mn>y.mn) r.mn=y.mn,r.mncnt=y.mncnt;
    else r.mn=x.mn,r.mncnt=x.mncnt+y.mncnt;
    if(x.mx>y.mx) r.mx=x.mx,r.mxcnt=x.mxcnt;
    else if(x.mx<y.mx) r.mx=y.mx,r.mxcnt=y.mxcnt;
    else r.mx=x.mx,r.mxcnt=x.mxcnt+y.mxcnt;
    return r;
}
S e(){return {INF,0,-INF,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.a>0) return {f.a*x.mn+f.b,x.mncnt,f.a*x.mx+f.b,x.mxcnt,x.len};
    if(f.a<0) return {f.a*x.mx+f.b,x.mxcnt,f.a*x.mn+f.b,x.mncnt,x.len};
    return {f.b,x.len,f.b,x.len,x.len};
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, 1, a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (個数 p.mncnt), 最大値 = p.mx (個数 p.mxcnt)
```

## 区間アフィン + 区間最小値の位置・最大値の位置

```cpp
const long long INF=1e18;
struct S{long long mn,mx; int imn,imx,l;};  // 最小値, 最大値, その最左位置, 区間の左端
struct F{long long a,b;};
S op(S x,S y){
    S r;
    if(x.mn<=y.mn) r.mn=x.mn,r.imn=x.imn; else r.mn=y.mn,r.imn=y.imn;
    if(x.mx>=y.mx) r.mx=x.mx,r.imx=x.imx; else r.mx=y.mx,r.imx=y.imx;
    r.l=std::min(x.l,y.l);
    return r;
}
S e(){return {INF,-INF,-1,-1,INT_MAX};}
S mapping(F f,S x){
    if(x.l==INT_MAX) return x;
    if(f.a>0) return {f.a*x.mn+f.b,f.a*x.mx+f.b,x.imn,x.imx,x.l};
    if(f.a<0) return {f.a*x.mx+f.b,f.a*x.mn+f.b,x.imx,x.imn,x.l};
    return {f.b,f.b,x.l,x.l,x.l};
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, a_i, i, i, i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (最左位置 p.imn), 最大値 = p.mx (最左位置 p.imx)
```

## 区間アフィン + ローリングハッシュ（回文判定つき）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const mint B=1000003;
struct S{mint h,rh,pw,geo;};  // pw = B^len, geo = 1+B+...+B^(len-1)
struct F{mint a,b;};
S op(S x,S y){
    return {x.h*y.pw+y.h, y.rh*x.pw+x.rh, x.pw*y.pw, x.geo*y.pw+y.geo};
}
S e(){return {0,0,1,0};}
S mapping(F f,S x){return {f.a*x.h+f.b*x.geo,f.a*x.rh+f.b*x.geo,x.pw,x.geo};}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {c_i, c_i, B, 1}
// 取得: auto p=seg.prod(l,r); ハッシュ = p.h, 回文 <=> p.h==p.rh
// 加算 v: {1,v}, 代入 v: {0,v}
```

## 区間アフィン + 隣接積和 Σ x_i x_{i+1} (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

struct S{mint sum,l,r,adj,len;};  // adj = Σ x_i x_{i+1}
struct F{mint a,b;};
S op(S x,S y){
    if(x.len==0) return y;
    if(y.len==0) return x;
    return {x.sum+y.sum,x.l,y.r,x.adj+y.adj+x.r*y.l,x.len+y.len};
}
S e(){return {0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    mint pairs=2*x.sum-x.l-x.r;  // Σ (x_i + x_{i+1})
    return {f.a*x.sum+f.b*x.len,f.a*x.l+f.b,f.a*x.r+f.b,
            f.a*f.a*x.adj+f.a*f.b*pairs+f.b*f.b*(x.len-1),x.len};
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); Σ x_i x_{i+1} = p.adj, 和 = p.sum
```

## 2 つの数列への区間アフィン + 区間積和 Σ a_i b_i

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

struct S{mint a,b,ab,len;};
struct F{mint pa,qa,pb,qb;};  // a_i ← pa a_i + qa, b_i ← pb b_i + qb
S op(S x,S y){return {x.a+y.a,x.b+y.b,x.ab+y.ab,x.len+y.len};}
S e(){return {0,0,0,0};}
S mapping(F f,S x){
    return {f.pa*x.a+f.qa*x.len,
            f.pb*x.b+f.qb*x.len,
            f.pa*f.pb*x.ab+f.pa*f.qb*x.a+f.qa*f.pb*x.b+f.qa*f.qb*x.len,
            x.len};
}
F composition(F f,F g){return {f.pa*g.pa,f.pa*g.qa+f.qa,f.pb*g.pb,f.pb*g.qb+f.qb};}
F id(){return {1,0,1,0};}
// 初期値: {a_i, b_i, a_i*b_i, 1}
// 取得: auto p=seg.prod(l,r); Σ a_i b_i = p.ab, Σ a_i = p.a, Σ b_i = p.b
// a に加算 v: {1,v,1,0}, a に代入 v: {0,v,1,0}, b に乗算 v: {1,0,v,0}
```

## 点の回転・反転・平行移動 + 座標の和・バウンディングボックス

```cpp
const long long INF=1e18;
struct S{long long sx,sy,len,mnx,mxx,mny,mxy;};
struct F{long long a,b,c,d,tx,ty;};  // (x,y) -> (a x + b y + tx, c x + d y + ty)
S op(S p,S q){
    return {p.sx+q.sx,p.sy+q.sy,p.len+q.len,
            std::min(p.mnx,q.mnx),std::max(p.mxx,q.mxx),std::min(p.mny,q.mny),std::max(p.mxy,q.mxy)};
}
S e(){return {0,0,0,INF,-INF,INF,-INF};}
S mapping(F f,S x){
    if(x.len==0) return x;
    auto lo=[&](long long u,long long v,long long t){return t+(u>=0?u*x.mnx:u*x.mxx)+(v>=0?v*x.mny:v*x.mxy);};
    auto hi=[&](long long u,long long v,long long t){return t+(u>=0?u*x.mxx:u*x.mnx)+(v>=0?v*x.mxy:v*x.mny);};
    return {f.a*x.sx+f.b*x.sy+f.tx*x.len,f.c*x.sx+f.d*x.sy+f.ty*x.len,x.len,
            lo(f.a,f.b,f.tx),hi(f.a,f.b,f.tx),lo(f.c,f.d,f.ty),hi(f.c,f.d,f.ty)};
}
F composition(F f,F g){
    return {f.a*g.a+f.b*g.c,f.a*g.b+f.b*g.d,f.c*g.a+f.d*g.c,f.c*g.b+f.d*g.d,
            f.a*g.tx+f.b*g.ty+f.tx,f.c*g.tx+f.d*g.ty+f.ty};
}
F id(){return {1,0,0,1,0,0};}
// 初期値: {x_i, y_i, 1, x_i, x_i, y_i, y_i}
// 取得: auto p=seg.prod(l,r); Σx = p.sx, Σy = p.sy, x の範囲 [p.mnx, p.mxx], y の範囲 [p.mny, p.mxy]
// 90 度回転: {0,-1,1,0,0,0}, x 軸で反転: {1,0,0,-1,0,0}, 平行移動: {1,0,0,1,dx,dy}, 拡大 k 倍: {k,0,0,k,0,0}
// バウンディングボックスは回転・反転・平行移動・拡大 (各行の非零が 1 つ) のときだけ正しい。和は任意の行列で正しい
```

## 区間乗算 + 区間和・最小値・最大値・二乗和・GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const long long INF=1e18;
struct S{long long sum,mn,mx; mint sq; long long l,r,g,len;};
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::min(a.mn,b.mn),std::max(a.mx,b.mx),a.sq+b.sq,
            a.l,b.r,std::gcd(std::gcd(a.g,b.g),std::abs(b.l-a.r)),a.len+b.len};
}
S e(){return {0,INF,-INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    long long p=f*x.mn,q=f*x.mx;
    return {f*x.sum,std::min(p,q),std::max(p,q),mint(f)*f*x.sq,f*x.l,f*x.r,std::abs(f)*x.g,x.len};
}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 最大値 = p.mx, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
```

## 区間アフィン + 区間和・最小値・最大値・二乗和・GCD

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const long long INF=1e18;
struct S{long long sum,mn,mx; mint sq; long long l,r,g,len;};
struct F{long long a,b;};
S op(S x,S y){
    if(x.len==0) return y;
    if(y.len==0) return x;
    return {x.sum+y.sum,std::min(x.mn,y.mn),std::max(x.mx,y.mx),x.sq+y.sq,
            x.l,y.r,std::gcd(std::gcd(x.g,y.g),std::abs(y.l-x.r)),x.len+y.len};
}
S e(){return {0,INF,-INF,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    long long p=f.a*x.mn+f.b,q=f.a*x.mx+f.b;
    mint a=f.a,b=f.b;
    return {f.a*x.sum+f.b*x.len,std::min(p,q),std::max(p,q),
            a*a*x.sq+2*a*b*x.sum+b*b*x.len,
            f.a*x.l+f.b,f.a*x.r+f.b,std::abs(f.a)*x.g,x.len};
}
F composition(F f,F g){return {f.a*g.a,f.a*g.b+f.b};}
F id(){return {1,0};}
// 初期値: {a_i, a_i, a_i, a_i*a_i, a_i, a_i, 0, 1}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 最大値 = p.mx, 二乗和 = p.sq, GCD = std::gcd(std::abs(p.l), p.g)
// 加算 v: {1,v}, 乗算 v: {v,0}, 代入 v: {0,v}
```

## 区間乗算 + 区間 GCD・LCM

```cpp
struct S{long long g,lc;};
using F=long long;
S op(S a,S b){return {std::gcd(a.g,b.g),std::lcm(a.lc,b.lc)};}
S e(){return {0,1};}
S mapping(F f,S x){return {std::abs(f)*x.g,std::abs(f)*x.lc};}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: {|a_i|, |a_i|}
// 取得: auto p=seg.prod(l,r); GCD = p.g, LCM = p.lc  (オーバーフローに注意)
```

## 区間乗算 + 区間 LCM

```cpp
using S=long long;
using F=long long;
S op(S a,S b){return std::lcm(a,b);}
S e(){return 1;}
S mapping(F f,S x){return std::abs(f)*x;}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: |a_i|
// 取得: LCM = seg.prod(l,r)  (オーバーフローに注意)
```

## 区間乗算 + 区間最小値・最大値とその個数・位置

```cpp
const long long INF=1e18;
struct S{long long mn,mncnt,mx,mxcnt; int imn,imx,lft; long long len;};  // imn, imx: 最左位置, lft: 区間の左端
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    S r=a; r.len=a.len+b.len;
    if(b.mx>a.mx) r.mx=b.mx,r.mxcnt=b.mxcnt,r.imx=b.imx;
    else if(b.mx==a.mx) r.mxcnt+=b.mxcnt;
    if(b.mn<a.mn) r.mn=b.mn,r.mncnt=b.mncnt,r.imn=b.imn;
    else if(b.mn==a.mn) r.mncnt+=b.mncnt;
    return r;
}
S e(){return {INF,0,-INF,0,-1,-1,-1,0};}
S mapping(F f,S x){
    if(x.len==0||f==1) return x;
    if(f==0) return {0,x.len,0,x.len,x.lft,x.lft,x.lft,x.len};
    if(f>0) return {f*x.mn,x.mncnt,f*x.mx,x.mxcnt,x.imn,x.imx,x.lft,x.len};
    return {f*x.mx,x.mxcnt,f*x.mn,x.mncnt,x.imx,x.imn,x.lft,x.len};
}
F composition(F f,F g){return f*g;}
F id(){return 1;}
// 初期値: {a_i, 1, a_i, 1, i, i, i, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (個数 p.mncnt, 最左位置 p.imn), 最大値 = p.mx (個数 p.mxcnt, 最左位置 p.imx)
```

# 5. 区間 chmin / chmax

## 区間 chmin + 区間最大値

```cpp
const long long INF=1e18;
using S=long long;
using F=long long;
S op(S a,S b){return std::max(a,b);}
S e(){return -INF;}
S mapping(F f,S x){return std::min(f,x);}
F composition(F f,F g){return std::min(f,g);}
F id(){return INF;}
// 取得: 最大値 = seg.prod(l,r)
```

## 区間 chmin + 区間最小値

```cpp
const long long INF=1e18;
using S=long long;
using F=long long;
S op(S a,S b){return std::min(a,b);}
S e(){return INF;}
S mapping(F f,S x){return std::min(f,x);}
F composition(F f,F g){return std::min(f,g);}
F id(){return INF;}
// 取得: 最小値 = seg.prod(l,r)
```

## 区間 chmin + 区間最小値とその個数

```cpp
const long long INF=1e18;
struct S{long long mn; long long cnt; long long len;};
using F=long long;
S op(S a,S b){
    if(a.mn<b.mn) return {a.mn,a.cnt,a.len+b.len};
    if(a.mn>b.mn) return {b.mn,b.cnt,a.len+b.len};
    return {a.mn,a.cnt+b.cnt,a.len+b.len};
}
S e(){return {INF,0,0};}
S mapping(F f,S x){return (x.len==0||f>x.mn)?x:S{f,x.len,x.len};}
F composition(F f,F g){return std::min(f,g);}
F id(){return INF;}
// 初期値: {a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 個数 = p.cnt
```

## 区間 chmin + 区間最小値・最大値

```cpp
const long long INF=1e18;
struct S{long long mn,mx;};
using F=long long;
S op(S a,S b){return {std::min(a.mn,b.mn),std::max(a.mx,b.mx)};}
S e(){return {INF,-INF};}
S mapping(F f,S x){return x.mn>x.mx?x:S{std::min(x.mn,f),std::min(x.mx,f)};}
F composition(F f,F g){return std::min(f,g);}
F id(){return INF;}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最大値 = p.mx
```

## 区間 chmin + 区間最小値の位置

```cpp
const long long INF=1e18;
struct S{long long mn; int idx; int l;};  // 最小値, その最左位置, 区間の左端
using F=long long;
S op(S a,S b){
    S r=a.mn<=b.mn?a:b;
    r.l=std::min(a.l,b.l);
    return r;
}
S e(){return {INF,INT_MAX,INT_MAX};}
S mapping(F f,S x){return (x.l==INT_MAX||f>x.mn)?x:S{f,x.l,x.l};}
F composition(F f,F g){return std::min(f,g);}
F id(){return INF;}
// 初期値: {a_i, i, i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最左位置 = p.idx
```

## 区間 chmax + 区間最大値

```cpp
const long long INF=1e18;
using S=long long;
using F=long long;
S op(S a,S b){return std::max(a,b);}
S e(){return -INF;}
S mapping(F f,S x){return std::max(f,x);}
F composition(F f,F g){return std::max(f,g);}
F id(){return -INF;}
// S, F を pair<値, 添字> にすれば最大値をとる添字も持てる (DP の復元など)
// 取得: 最大値 = seg.prod(l,r)
```

## 区間 chmax + 区間最小値

```cpp
const long long INF=1e18;
using S=long long;
using F=long long;
S op(S a,S b){return std::min(a,b);}
S e(){return INF;}
S mapping(F f,S x){return std::max(f,x);}
F composition(F f,F g){return std::max(f,g);}
F id(){return -INF;}
// 取得: 最小値 = seg.prod(l,r)
```

## 区間 chmax + 区間最大値とその個数

```cpp
const long long INF=1e18;
struct S{long long mx; long long cnt; long long len;};
using F=long long;
S op(S a,S b){
    if(a.mx>b.mx) return {a.mx,a.cnt,a.len+b.len};
    if(a.mx<b.mx) return {b.mx,b.cnt,a.len+b.len};
    return {a.mx,a.cnt+b.cnt,a.len+b.len};
}
S e(){return {-INF,0,0};}
S mapping(F f,S x){return (x.len==0||f<x.mx)?x:S{f,x.len,x.len};}
F composition(F f,F g){return std::max(f,g);}
F id(){return -INF;}
// 初期値: {a_i, 1, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 個数 = p.cnt
```

## 区間 chmax + 区間最小値・最大値

```cpp
const long long INF=1e18;
struct S{long long mn,mx;};
using F=long long;
S op(S a,S b){return {std::min(a.mn,b.mn),std::max(a.mx,b.mx)};}
S e(){return {INF,-INF};}
S mapping(F f,S x){return x.mn>x.mx?x:S{std::max(x.mn,f),std::max(x.mx,f)};}
F composition(F f,F g){return std::max(f,g);}
F id(){return -INF;}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最大値 = p.mx
```

## 区間 chmax + 区間最大値の位置

```cpp
const long long INF=1e18;
struct S{long long mx; int idx; int l;};  // 最大値, その最左位置, 区間の左端
using F=long long;
S op(S a,S b){
    S r=a.mx>=b.mx?a:b;
    r.l=std::min(a.l,b.l);
    return r;
}
S e(){return {-INF,INT_MAX,INT_MAX};}
S mapping(F f,S x){return (x.l==INT_MAX||f<x.mx)?x:S{f,x.l,x.l};}
F composition(F f,F g){return std::max(f,g);}
F id(){return -INF;}
// 初期値: {a_i, i, i}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx, 最左位置 = p.idx
```

## 区間加算・chmin・chmax・代入 + 区間最小値・最大値

```cpp
const long long INF=1e18;
struct S{long long mn; long long mx;};
struct F{long long add,lo,hi;};  // x -> min(max(x+add, lo), hi)
long long clamp_(long long x,long long lo,long long hi){return std::min(std::max(x,lo),hi);}
S op(S x,S y){return {std::min(x.mn,y.mn),std::max(x.mx,y.mx)};}
S e(){return {INF,-INF};}
S mapping(F f,S x){
    if(x.mn>x.mx) return x;
    return {clamp_(x.mn+f.add,f.lo,f.hi),clamp_(x.mx+f.add,f.lo,f.hi)};
}
F composition(F f,F g){
    return {g.add+f.add,
            clamp_(g.lo+f.add,f.lo,f.hi),
            clamp_(g.hi+f.add,f.lo,f.hi)};
}
F id(){return {0,-INF,INF};}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最大値 = p.mx
// 加算 v: {v,-INF,INF}, chmin v: {0,-INF,v}, chmax v: {0,v,INF}, 代入 v: {0,v,v}
```

## 区間 chmin + 区間最小値とその個数・位置・最大値

```cpp
const long long INF=1e18;
struct S{long long mn,cnt,mx; int idx,lft; long long len;};  // idx: 最小値の最左位置, lft: 区間の左端
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    S r=a; r.len=a.len+b.len; r.mx=std::max(a.mx,b.mx);
    if(b.mn<a.mn) r.mn=b.mn,r.cnt=b.cnt,r.idx=b.idx;
    else if(b.mn==a.mn) r.cnt+=b.cnt;
    return r;
}
S e(){return {INF,0,-INF,-1,-1,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.mx=std::min(x.mx,f);
    if(f<=x.mn) x.mn=f,x.cnt=x.len,x.idx=x.lft;
    return x;
}
F composition(F f,F g){return std::min(f,g);}
F id(){return INF;}
// 初期値: {a_i, 1, a_i, i, i, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (個数 p.cnt, 最左位置 p.idx), 最大値 = p.mx
```

## 区間 chmax + 区間最大値とその個数・位置・最小値

```cpp
const long long INF=1e18;
struct S{long long mx,cnt,mn; int idx,lft; long long len;};  // idx: 最大値の最左位置, lft: 区間の左端
using F=long long;
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    S r=a; r.len=a.len+b.len; r.mn=std::min(a.mn,b.mn);
    if(b.mx>a.mx) r.mx=b.mx,r.cnt=b.cnt,r.idx=b.idx;
    else if(b.mx==a.mx) r.cnt+=b.cnt;
    return r;
}
S e(){return {-INF,0,INF,-1,-1,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    x.mn=std::max(x.mn,f);
    if(f>=x.mx) x.mx=f,x.cnt=x.len,x.idx=x.lft;
    return x;
}
F composition(F f,F g){return std::max(f,g);}
F id(){return -INF;}
// 初期値: {a_i, 1, a_i, i, i, 1}
// 取得: auto p=seg.prod(l,r); 最大値 = p.mx (個数 p.cnt, 最左位置 p.idx), 最小値 = p.mn
```

## 区間アフィン・chmin・chmax・代入 + 区間最小値・最大値

```cpp
const long long INF=1e18;
struct S{long long mn,mx;};
struct F{long long a,b,lo,hi;};  // x -> min(max(a x + b, lo), hi)
long long clamp_(__int128 x,long long lo,long long hi){return (long long)std::min<__int128>(std::max<__int128>(x,lo),hi);}
S op(S x,S y){return {std::min(x.mn,y.mn),std::max(x.mx,y.mx)};}
S e(){return {INF,-INF};}
S mapping(F f,S x){
    if(x.mn>x.mx) return x;
    long long p=clamp_((__int128)f.a*x.mn+f.b,f.lo,f.hi),q=clamp_((__int128)f.a*x.mx+f.b,f.lo,f.hi);
    return {std::min(p,q),std::max(p,q)};
}
F composition(F f,F g){
    __int128 L=(__int128)f.a*g.lo+f.b,H=(__int128)f.a*g.hi+f.b;
    if(f.a<0) std::swap(L,H);
    return {f.a*g.a,f.a*g.b+f.b,clamp_(L,f.lo,f.hi),clamp_(H,f.lo,f.hi)};
}
F id(){return {1,0,-INF,INF};}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn, 最大値 = p.mx
// 加算 v: {1,v,-INF,INF}, 乗算 v: {v,0,-INF,INF}, chmin v: {1,0,-INF,v}, chmax v: {1,0,v,INF}, 代入 v: {0,v,-INF,INF}
```

# 6. 区間に添字の関数を加算・代入

## 等差数列加算 + 区間和

```cpp
struct S{long long sum; long long len; long long isum;};
struct F{long long a; long long b;};  // x_i += a + b*i
S op(S x,S y){return {x.sum+y.sum,x.len+y.len,x.isum+y.isum};}
S e(){return {0,0,0};}
S mapping(F f,S x){return {x.sum+f.a*x.len+f.b*x.isum,x.len,x.isum};}
F composition(F f,F g){return {f.a+g.a,f.b+g.b};}
F id(){return {0,0};}
// 初期値: {a_i, 1, i}
// 取得: auto p=seg.prod(l,r); 和 = p.sum
// [l,r) に c, c+d, c+2d, ... を加算: seg.apply(l,r,{c-d*l,d})
```

## 等差数列加算・等差数列代入 + 区間和

```cpp
struct S{long long sum; long long len; long long isum;};
struct F{bool upd; long long a; long long b;};  // upd ? x_i = a + b*i : x_i += a + b*i
S op(S x,S y){return {x.sum+y.sum,x.len+y.len,x.isum+y.isum};}
S e(){return {0,0,0};}
S mapping(F f,S x){return {(f.upd?0:x.sum)+f.a*x.len+f.b*x.isum,x.len,x.isum};}
F composition(F f,F g){return f.upd?f:F{g.upd,g.a+f.a,g.b+f.b};}
F id(){return {false,0,0};}
// 初期値: {a_i, 1, i}
// 取得: auto p=seg.prod(l,r); 和 = p.sum
// [l,r) に c, c+d, c+2d, ... を加算: {false,c-d*l,d}, 代入: {true,c-d*l,d}
```

## 等差数列代入 + 区間和・最小値・最大値

```cpp
const long long INF=1e18;
struct S{long long sum,mn,mx,len,isum,lo,hi;};  // lo, hi: 区間の左端・右端の添字
struct F{bool upd; long long a; long long b;};  // x_i = a + b*i
S op(S x,S y){
    if(x.len==0) return y;
    if(y.len==0) return x;
    return {x.sum+y.sum,std::min(x.mn,y.mn),std::max(x.mx,y.mx),x.len+y.len,x.isum+y.isum,x.lo,y.hi};
}
S e(){return {0,INF,-INF,0,0,0,0};}
S mapping(F f,S x){
    if(!f.upd||x.len==0) return x;
    long long p=f.a+f.b*x.lo,q=f.a+f.b*x.hi;
    return {f.a*x.len+f.b*x.isum,std::min(p,q),std::max(p,q),x.len,x.isum,x.lo,x.hi};
}
F composition(F f,F g){return f.upd?f:g;}
F id(){return {false,0,0};}
// 初期値: {a_i, a_i, a_i, 1, i, i, i}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 最大値 = p.mx
// [l,r) に c, c+d, c+2d, ... を代入: {true,c-d*l,d}
```

## 二次式加算 + 区間和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint sum,s0,s1,s2;};  // s0 = Σ1, s1 = Σi, s2 = Σi^2
struct F{mint a,b,c;};  // x_i += a + b*i + c*i^2
S op(S x,S y){return {x.sum+y.sum,x.s0+y.s0,x.s1+y.s1,x.s2+y.s2};}
S e(){return {0,0,0,0};}
S mapping(F f,S x){return {x.sum+f.a*x.s0+f.b*x.s1+f.c*x.s2,x.s0,x.s1,x.s2};}
F composition(F f,F g){return {f.a+g.a,f.b+g.b,f.c+g.c};}
F id(){return {0,0,0};}
// 初期値: {a_i, 1, i, i*i}
// 取得: auto p=seg.prod(l,r); 和 = p.sum
// [l,r) に p + q(i-l) + s(i-l)^2 を加算: {p-q*l+s*l*l, q-2*s*l, s}
```

## 等比数列加算 + 区間和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const mint R=2;  // 公比
struct S{mint sum,rs;};  // rs = Σ R^i
using F=mint;  // x_i += f * R^i
S op(S x,S y){return {x.sum+y.sum,x.rs+y.rs};}
S e(){return {0,0};}
S mapping(F f,S x){return {x.sum+f*x.rs,x.rs};}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, R^i}
// 取得: auto p=seg.prod(l,r); 和 = p.sum
// [l,r) に c, cR, cR^2, ... を加算: c*R.inv().pow(l)
```

## フィボナッチ数列加算 + 区間和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
struct S{mint sum,f0,f1;};  // f0 = Σ Fib_i, f1 = Σ Fib_{i+1}
struct F{mint a,b;};  // x_i += a*Fib_i + b*Fib_{i+1}
S op(S x,S y){return {x.sum+y.sum,x.f0+y.f0,x.f1+y.f1};}
S e(){return {0,0,0};}
S mapping(F f,S x){return {x.sum+f.a*x.f0+f.b*x.f1,x.f0,x.f1};}
F composition(F f,F g){return {f.a+g.a,f.b+g.b};}
F id(){return {0,0};}
// Fib_0=0, Fib_1=1, Fib_{-n} = (-1)^{n+1} Fib_n
// 初期値: {a_i, Fib_i, Fib_{i+1}}
// 取得: auto p=seg.prod(l,r); 和 = p.sum
// [l,r) に Fib_1, Fib_2, Fib_3, ... を加算: {Fib_{-l}, Fib_{1-l}}
```

## 等差数列加算 + 区間二乗和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

struct S{mint sum,sq,ix,s0,s1,s2;};  // ix = Σ i x_i, s0 = Σ1, s1 = Σi, s2 = Σi^2
struct F{mint a,b;};  // x_i += a + b*i
S op(S x,S y){return {x.sum+y.sum,x.sq+y.sq,x.ix+y.ix,x.s0+y.s0,x.s1+y.s1,x.s2+y.s2};}
S e(){return {0,0,0,0,0,0};}
S mapping(F f,S x){
    mint a=f.a,b=f.b;
    return {x.sum+a*x.s0+b*x.s1,
            x.sq+2*a*x.sum+2*b*x.ix+a*a*x.s0+2*a*b*x.s1+b*b*x.s2,
            x.ix+a*x.s1+b*x.s2,
            x.s0,x.s1,x.s2};
}
F composition(F f,F g){return {f.a+g.a,f.b+g.b};}
F id(){return {0,0};}
// 初期値: {a_i, a_i*a_i, i*a_i, 1, i, i*i}
// 取得: auto p=seg.prod(l,r); 二乗和 = p.sq, 和 = p.sum
// [l,r) に c, c+d, c+2d, ... を加算: {c-d*l, d}
```

## 任意の基底関数の線形結合を加算 + 区間和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=3;  // 基底関数の個数
struct S{mint sum; mint phi[K];};  // phi[k] = Σ φ_k(i)
struct F{mint c[K];};  // x_i += Σ c[k] φ_k(i)
S op(S x,S y){x.sum+=y.sum; for(int k=0;k<K;k++) x.phi[k]+=y.phi[k]; return x;}
S e(){return S{};}
S mapping(F f,S x){for(int k=0;k<K;k++) x.sum+=f.c[k]*x.phi[k]; return x;}
F composition(F f,F g){for(int k=0;k<K;k++) f.c[k]+=g.c[k]; return f;}
F id(){return F{};}
// 初期値: sum = a_i, phi[k] = φ_k(i)
// 取得: auto p=seg.prod(l,r); 和 = p.sum
// 例: φ = (1, i, i^2, i^3), (R^i, i R^i), (Fib_i, Fib_{i+1}), (sin, cos) など
```

## 等差数列加算・等差数列代入 + 等差数列判定・公差・区間 GCD

```cpp
struct S{long long l,r,fd,ld,g,len,lo,hi;};  // 左端の値, 右端の値, 最初と最後の隣接差, 隣接差の差の GCD, 長さ, 左端・右端の添字
struct F{bool upd; long long a,b;};  // upd ? x_i = a + b*i : x_i += a + b*i
S op(S x,S y){
    if(x.len==0) return y;
    if(y.len==0) return x;
    long long m=y.l-x.r,g=std::gcd(x.g,y.g);
    if(x.len>=2) g=std::gcd(g,std::abs(m-x.ld));
    if(y.len>=2) g=std::gcd(g,std::abs(y.fd-m));
    return {x.l,y.r,x.len>=2?x.fd:m,y.len>=2?y.ld:m,g,x.len+y.len,x.lo,y.hi};
}
S e(){return {0,0,0,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.upd) return {f.a+f.b*x.lo,f.a+f.b*x.hi,f.b,f.b,0,x.len,x.lo,x.hi};
    return {x.l+f.a+f.b*x.lo,x.r+f.a+f.b*x.hi,x.fd+f.b,x.ld+f.b,x.g,x.len,x.lo,x.hi};
}
F composition(F f,F g){return f.upd?f:F{g.upd,g.a+f.a,g.b+f.b};}
F id(){return {false,0,0};}
// 初期値: {a_i, a_i, 0, 0, 0, 1, i, i}
// 取得: auto p=seg.prod(l,r); 等差数列 <=> p.g==0, 公差 = p.fd
// [l,r) に c, c+d, c+2d, ... を加算: {false,c-d*l,d}, 代入: {true,c-d*l,d}
```

## 添字の偶奇で別々に加算 + 偶奇別の和・最大値

```cpp
const long long INF=1e18;
struct S{long long sum[2],mx[2],cnt[2];};  // [p]: 添字の偶奇が p の要素について
using F=std::array<long long,2>;  // 添字が偶数の要素に f[0]、奇数の要素に f[1] を加算
S op(S a,S b){
    S r;
    for(int p=0;p<2;p++){r.sum[p]=a.sum[p]+b.sum[p]; r.mx[p]=std::max(a.mx[p],b.mx[p]); r.cnt[p]=a.cnt[p]+b.cnt[p];}
    return r;
}
S e(){return {{0,0},{-INF,-INF},{0,0}};}
S mapping(F f,S x){
    for(int p=0;p<2;p++) if(x.cnt[p]){x.sum[p]+=f[p]*x.cnt[p]; x.mx[p]+=f[p];}
    return x;
}
F composition(F f,F g){return {f[0]+g[0],f[1]+g[1]};}
F id(){return {0,0};}
// 初期値: p = i%2 -> sum[p]=a_i, mx[p]=a_i, cnt[p]=1, 他方は {0,-INF,0}
// 取得: auto p=seg.prod(l,r); 添字が偶数の要素の和 = p.sum[0], 最大値 = p.mx[0] (奇数は [1]), 交互和 = p.sum[0]-p.sum[1]
```

## 任意の基底関数の線形結合を加算・代入 + 区間和 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=3;  // 基底関数の個数
struct S{mint sum; mint phi[K];};  // phi[k] = Σ φ_k(i)
struct F{bool upd; mint c[K];};  // upd ? x_i = Σ c[k] φ_k(i) : x_i += Σ c[k] φ_k(i)
S op(S x,S y){x.sum+=y.sum; for(int k=0;k<K;k++) x.phi[k]+=y.phi[k]; return x;}
S e(){return S{};}
S mapping(F f,S x){
    if(f.upd) x.sum=0;
    for(int k=0;k<K;k++) x.sum+=f.c[k]*x.phi[k];
    return x;
}
F composition(F f,F g){
    if(f.upd) return f;
    for(int k=0;k<K;k++) g.c[k]+=f.c[k];
    return g;
}
F id(){return F{};}
// 初期値: sum = a_i, phi[k] = φ_k(i)
// 取得: auto p=seg.prod(l,r); 和 = p.sum
```

# 7. 区間符号反転 (x ← -x)

## 区間和・最小値・最大値

```cpp
const long long INF=1e18;
struct S{long long sum,mn,mx;};
using F=bool;
S op(S a,S b){return {a.sum+b.sum,std::min(a.mn,b.mn),std::max(a.mx,b.mx)};}
S e(){return {0,INF,-INF};}
S mapping(F f,S x){return f?S{-x.sum,-x.mx,-x.mn}:x;}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: {a_i, a_i, a_i}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn, 最大値 = p.mx
```

## 区間最大部分和・最小部分和

```cpp
const long long INF=1e18;
struct S{long long sum,premx,premn,sufmx,sufmn,bestmx,bestmn;};
using F=bool;
S op(S a,S b){
    return {a.sum+b.sum,
            std::max(a.premx,a.sum+b.premx),
            std::min(a.premn,a.sum+b.premn),
            std::max(b.sufmx,b.sum+a.sufmx),
            std::min(b.sufmn,b.sum+a.sufmn),
            std::max({a.bestmx,b.bestmx,a.sufmx+b.premx}),
            std::min({a.bestmn,b.bestmn,a.sufmn+b.premn})};
}
S e(){return {0,-INF,INF,-INF,INF,-INF,INF};}
S mapping(F f,S x){
    if(!f) return x;
    return {-x.sum,-x.premn,-x.premx,-x.sufmn,-x.sufmx,-x.bestmn,-x.bestmx};
}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: {a_i, a_i, a_i, a_i, a_i, a_i, a_i}
// 取得: auto p=seg.prod(l,r); 最大部分和 = p.bestmx, 最小部分和 = p.bestmn
```

## 区間最小値と個数・最大値と個数

```cpp
const long long INF=1e18;
struct S{long long mn,mncnt,mx,mxcnt;};
using F=bool;
S op(S x,S y){
    S r;
    if(x.mn<y.mn) r.mn=x.mn,r.mncnt=x.mncnt;
    else if(x.mn>y.mn) r.mn=y.mn,r.mncnt=y.mncnt;
    else r.mn=x.mn,r.mncnt=x.mncnt+y.mncnt;
    if(x.mx>y.mx) r.mx=x.mx,r.mxcnt=x.mxcnt;
    else if(x.mx<y.mx) r.mx=y.mx,r.mxcnt=y.mxcnt;
    else r.mx=x.mx,r.mxcnt=x.mxcnt+y.mxcnt;
    return r;
}
S e(){return {INF,0,-INF,0};}
S mapping(F f,S x){return f?S{-x.mx,x.mxcnt,-x.mn,x.mncnt}:x;}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: {a_i, 1, a_i, 1}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (個数 p.mncnt), 最大値 = p.mx (個数 p.mxcnt)
```

## 区間最小値の位置・最大値の位置

```cpp
const long long INF=1e18;
struct S{long long mn,mx; int imn,imx;};
using F=bool;
S op(S x,S y){
    S r;
    if(x.mn<=y.mn) r.mn=x.mn,r.imn=x.imn; else r.mn=y.mn,r.imn=y.imn;
    if(x.mx>=y.mx) r.mx=x.mx,r.imx=x.imx; else r.mx=y.mx,r.imx=y.imx;
    return r;
}
S e(){return {INF,-INF,-1,-1};}
S mapping(F f,S x){return f?S{-x.mx,-x.mn,x.imx,x.imn}:x;}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: {a_i, a_i, i, i}
// 取得: auto p=seg.prod(l,r); 最小値 = p.mn (最左位置 p.imn), 最大値 = p.mx (最左位置 p.imx)
```

## 区間和・最小値・最大値とその個数・位置・最大部分和・最小部分和

```cpp
const long long INF=1e18;
struct S{long long sum,mn,mncnt,mx,mxcnt,premx,premn,sufmx,sufmn,bestmx,bestmn; int imn,imx;};
using F=bool;
S op(S a,S b){
    S r;
    r.sum=a.sum+b.sum;
    if(a.mn<b.mn) r.mn=a.mn,r.mncnt=a.mncnt,r.imn=a.imn;
    else if(a.mn>b.mn) r.mn=b.mn,r.mncnt=b.mncnt,r.imn=b.imn;
    else r.mn=a.mn,r.mncnt=a.mncnt+b.mncnt,r.imn=a.imn;
    if(a.mx>b.mx) r.mx=a.mx,r.mxcnt=a.mxcnt,r.imx=a.imx;
    else if(a.mx<b.mx) r.mx=b.mx,r.mxcnt=b.mxcnt,r.imx=b.imx;
    else r.mx=a.mx,r.mxcnt=a.mxcnt+b.mxcnt,r.imx=a.imx;
    r.premx=std::max(a.premx,a.sum+b.premx);
    r.premn=std::min(a.premn,a.sum+b.premn);
    r.sufmx=std::max(b.sufmx,b.sum+a.sufmx);
    r.sufmn=std::min(b.sufmn,b.sum+a.sufmn);
    r.bestmx=std::max({a.bestmx,b.bestmx,a.sufmx+b.premx});
    r.bestmn=std::min({a.bestmn,b.bestmn,a.sufmn+b.premn});
    return r;
}
S e(){return {0,INF,0,-INF,0,-INF,INF,-INF,INF,-INF,INF,INT_MAX,INT_MAX};}
S mapping(F f,S x){
    if(!f) return x;
    return {-x.sum,-x.mx,x.mxcnt,-x.mn,x.mncnt,-x.premn,-x.premx,-x.sufmn,-x.sufmx,-x.bestmn,-x.bestmx,x.imx,x.imn};
}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: {a_i, a_i, 1, a_i, 1, a_i, a_i, a_i, a_i, a_i, a_i, i, i}
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最小値 = p.mn (個数 p.mncnt, 最左位置 p.imn), 最大値 = p.mx (個数 p.mxcnt, 最左位置 p.imx), 最大部分和 = p.bestmx, 最小部分和 = p.bestmn
```

## 区間積・GCD・LCM

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

struct S{mint prod; long long len,g,lc;};  // g, lc は |x_i| について
using F=bool;
S op(S a,S b){return {a.prod*b.prod,a.len+b.len,std::gcd(a.g,b.g),std::lcm(a.lc,b.lc)};}
S e(){return {1,0,0,1};}
S mapping(F f,S x){
    if(f&&(x.len&1)) x.prod=-x.prod;
    return x;
}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: {a_i, 1, |a_i|, |a_i|}
// 取得: auto p=seg.prod(l,r); 積 = p.prod, GCD = p.g, LCM = p.lc
```

# 8. 区間 0/1 反転・代入

## 反転 + 1 の個数

```cpp
struct S{long long one; long long len;};
using F=bool;
S op(S a,S b){return {a.one+b.one,a.len+b.len};}
S e(){return {0,0};}
S mapping(F f,S x){return f?S{x.len-x.one,x.len}:x;}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); 1 の個数 = p.one
```

## 反転 + 転倒数

```cpp
struct S{long long zero,one,inv;};
using F=bool;
S op(S a,S b){return {a.zero+b.zero,a.one+b.one,a.inv+b.inv+a.one*b.zero};}
S e(){return {0,0,0};}
S mapping(F f,S x){return f?S{x.one,x.zero,x.zero*x.one-x.inv}:x;}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: 0 -> {1,0,0}, 1 -> {0,1,0}
// 取得: auto p=seg.prod(l,r); 転倒数 = p.inv
```

## 反転 + 最長連続 0 / 1

```cpp
struct S{long long len,pre[2],suf[2],best[2];};
using F=bool;
S op(S a,S b){
    S r; r.len=a.len+b.len;
    for(int c=0;c<2;c++){
        r.pre[c]=a.pre[c]==a.len?a.len+b.pre[c]:a.pre[c];
        r.suf[c]=b.suf[c]==b.len?b.len+a.suf[c]:b.suf[c];
        r.best[c]=std::max({a.best[c],b.best[c],a.suf[c]+b.pre[c]});
    }
    return r;
}
S e(){return {0,{0,0},{0,0},{0,0}};}
S mapping(F f,S x){
    if(f){std::swap(x.pre[0],x.pre[1]);std::swap(x.suf[0],x.suf[1]);std::swap(x.best[0],x.best[1]);}
    return x;
}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: 0 -> {1,{1,0},{1,0},{1,0}}, 1 -> {1,{0,1},{0,1},{0,1}}
// 取得: auto p=seg.prod(l,r); 最長連続 0 = p.best[0], 最長連続 1 = p.best[1]
```

## 反転・代入 + 1 の個数・転倒数・最長連続 0 / 1

```cpp
struct S{long long len,cnt[2],inv,pre[2],suf[2],best[2];};
struct F{int to[2];};  // 0 -> to[0], 1 -> to[1]
S op(S a,S b){
    S r; r.len=a.len+b.len; r.inv=a.inv+b.inv+a.cnt[1]*b.cnt[0];
    for(int c=0;c<2;c++){
        r.cnt[c]=a.cnt[c]+b.cnt[c];
        r.pre[c]=a.pre[c]==a.len?a.len+b.pre[c]:a.pre[c];
        r.suf[c]=b.suf[c]==b.len?b.len+a.suf[c]:b.suf[c];
        r.best[c]=std::max({a.best[c],b.best[c],a.suf[c]+b.pre[c]});
    }
    return r;
}
S e(){return S{};}
S mapping(F f,S x){
    if(f.to[0]==0&&f.to[1]==1) return x;
    if(f.to[0]==1&&f.to[1]==0){
        std::swap(x.cnt[0],x.cnt[1]); x.inv=x.cnt[0]*x.cnt[1]-x.inv;
        std::swap(x.pre[0],x.pre[1]); std::swap(x.suf[0],x.suf[1]); std::swap(x.best[0],x.best[1]);
        return x;
    }
    int c=f.to[0]; S r{}; r.len=x.len;
    r.cnt[c]=r.pre[c]=r.suf[c]=r.best[c]=x.len;
    return r;
}
F composition(F f,F g){return {{f.to[g.to[0]],f.to[g.to[1]]}};}
F id(){return {{0,1}};}
// 初期値: c -> len=1, cnt[c]=pre[c]=suf[c]=best[c]=1, 他は 0
// 取得: auto p=seg.prod(l,r); 1 の個数 = p.cnt[1], 転倒数 = p.inv, 最長連続 c = p.best[c]
// 反転: {{1,0}}, 0 を代入: {{0,0}}, 1 を代入: {{1,1}}
```

## 反転・代入 + ローリングハッシュ（回文判定つき）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const mint B=1000003;
struct S{mint h,rh,pw,geo;};  // pw = B^len, geo = 1+B+...+B^(len-1)
struct F{int to[2];};  // 0 -> to[0], 1 -> to[1]
S op(S a,S b){
    return {a.h*b.pw+b.h, b.rh*a.pw+a.rh, a.pw*b.pw, a.geo*b.pw+b.geo};
}
S e(){return {0,0,1,0};}
S mapping(F f,S x){
    if(f.to[0]==0&&f.to[1]==1) return x;
    if(f.to[0]==1&&f.to[1]==0) return {x.geo-x.h,x.geo-x.rh,x.pw,x.geo};
    mint v=f.to[0]*x.geo;
    return {v,v,x.pw,x.geo};
}
F composition(F f,F g){return {{f.to[g.to[0]],f.to[g.to[1]]}};}
F id(){return {{0,1}};}
// 初期値: {a_i, a_i, B, 1}
// 取得: auto p=seg.prod(l,r); ハッシュ = p.h, 回文 <=> p.h==p.rh
// B=2 にすると h は 2 進数として読んだ値 (mod)
// 反転: {{1,0}}, 0 を代入: {{0,0}}, 1 を代入: {{1,1}}
```

## 反転・代入 + ランの数・最長の交互列 (0101...)

```cpp
struct S{long long len,lv,rv,runs,pre,suf,best;};  // best: x_i != x_{i+1} が続く最長
struct F{int to[2];};  // 0 -> to[0], 1 -> to[1]
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    bool c=a.rv!=b.lv;
    return {a.len+b.len,a.lv,b.rv,a.runs+b.runs-!c,
            (c&&a.pre==a.len)?a.len+b.pre:a.pre,
            (c&&b.suf==b.len)?b.len+a.suf:b.suf,
            std::max({a.best,b.best,c?a.suf+b.pre:0})};
}
S e(){return {0,0,0,0,0,0,0};}
S mapping(F f,S x){
    if(x.len==0) return x;
    if(f.to[0]!=f.to[1]){x.lv=f.to[x.lv]; x.rv=f.to[x.rv]; return x;}
    return {x.len,f.to[0],f.to[0],1,1,1,1};
}
F composition(F f,F g){return {{f.to[g.to[0]],f.to[g.to[1]]}};}
F id(){return {{0,1}};}
// 初期値: {1, a_i, a_i, 1, 1, 1, 1}
// 取得: auto p=seg.prod(l,r); ランの数 = p.runs, 最長の交互列 = p.best
// 反転: {{1,0}}, 0 を代入: {{0,0}}, 1 を代入: {{1,1}}
```

## 反転・代入 + 最長の広義単調部分列（連続でなくてよい）

```cpp
struct S{long long c[2],inc,dec;};  // inc: 最長の広義増加部分列 (0..01..1), dec: 最長の広義減少部分列
struct F{int to[2];};  // 0 -> to[0], 1 -> to[1]
S op(S a,S b){
    return {{a.c[0]+b.c[0],a.c[1]+b.c[1]},
            std::max(a.c[0]+b.inc,a.inc+b.c[1]),
            std::max(a.c[1]+b.dec,a.dec+b.c[0])};
}
S e(){return {{0,0},0,0};}
S mapping(F f,S x){
    if(f.to[0]==0&&f.to[1]==1) return x;
    if(f.to[0]==1&&f.to[1]==0) return {{x.c[1],x.c[0]},x.dec,x.inc};
    long long n=x.c[0]+x.c[1];
    return f.to[0]==0?S{{n,0},n,n}:S{{0,n},n,n};
}
F composition(F f,F g){return {{f.to[g.to[0]],f.to[g.to[1]]}};}
F id(){return {{0,1}};}
// 初期値: 0 -> {{1,0},1,1}, 1 -> {{0,1},1,1}
// 取得: auto p=seg.prod(l,r); 最長の広義増加部分列 = p.inc, 最長の広義減少部分列 = p.dec
// 反転: {{1,0}}, 0 を代入: {{0,0}}, 1 を代入: {{1,1}}
```

## 反転・代入 + 1 の個数・1 の位置の和

```cpp
struct S{long long cnt[2],pos[2];};  // cnt[c]: c の個数, pos[c]: c である位置 i の和
struct F{int to[2];};  // 0 -> to[0], 1 -> to[1]
S op(S a,S b){return {{a.cnt[0]+b.cnt[0],a.cnt[1]+b.cnt[1]},{a.pos[0]+b.pos[0],a.pos[1]+b.pos[1]}};}
S e(){return {{0,0},{0,0}};}
S mapping(F f,S x){
    S r{};
    for(int c=0;c<2;c++){r.cnt[f.to[c]]+=x.cnt[c]; r.pos[f.to[c]]+=x.pos[c];}
    return r;
}
F composition(F f,F g){return {{f.to[g.to[0]],f.to[g.to[1]]}};}
F id(){return {{0,1}};}
// 初期値: cnt[a_i]=1, pos[a_i]=i
// 取得: auto p=seg.prod(l,r); 1 の個数 = p.cnt[1], 1 の位置の和 = p.pos[1]
// 反転: {{1,0}}, 0 を代入: {{0,0}}, 1 を代入: {{1,1}}
// k 番目の 1 の位置は max_right で cnt[1] < k となる最大の右端
```

# 9. 区間の値の置換（値域が小さいとき）

## x ← to[x] + 各値の個数・区間和

```cpp
const int K=3;  // 値は 0..K-1
struct S{long long cnt[K];};
struct F{int to[K];};
S op(S a,S b){for(int v=0;v<K;v++) a.cnt[v]+=b.cnt[v]; return a;}
S e(){return S{};}
S mapping(F f,S x){
    S r{};
    for(int v=0;v<K;v++) r.cnt[f.to[v]]+=x.cnt[v];
    return r;
}
F composition(F f,F g){F h; for(int v=0;v<K;v++) h.to[v]=f.to[g.to[v]]; return h;}
F id(){F h; for(int v=0;v<K;v++) h.to[v]=v; return h;}
// 初期値: cnt[a_i]=1
// 取得: auto p=seg.prod(l,r); 値 v の個数 = p.cnt[v], 和 = Σ v*p.cnt[v]
// 和 = Σ v*cnt[v], 二乗和 = Σ v*v*cnt[v], 最大値 = cnt[v]>0 となる最大の v
// +d (mod K): to[v]=(v+d)%K, 代入 c: to[v]=c, a を b に置換: to[a]=b
// 区間ソート: cnt を取って、小さい値から順に連続する区間へ代入
```

## x ← to[x] + 転倒数

```cpp
const int K=3;  // 値は 0..K-1
struct S{long long cnt[K]; long long inv[K][K];};  // inv[u][v]: i<j, x_i=u, x_j=v の組の数
struct F{int to[K];};
S op(S a,S b){
    S r{};
    for(int u=0;u<K;u++){
        r.cnt[u]=a.cnt[u]+b.cnt[u];
        for(int v=0;v<K;v++) r.inv[u][v]=a.inv[u][v]+b.inv[u][v]+a.cnt[u]*b.cnt[v];
    }
    return r;
}
S e(){return S{};}
S mapping(F f,S x){
    S r{};
    for(int u=0;u<K;u++){
        r.cnt[f.to[u]]+=x.cnt[u];
        for(int v=0;v<K;v++) r.inv[f.to[u]][f.to[v]]+=x.inv[u][v];
    }
    return r;
}
F composition(F f,F g){F h; for(int v=0;v<K;v++) h.to[v]=f.to[g.to[v]]; return h;}
F id(){F h; for(int v=0;v<K;v++) h.to[v]=v; return h;}
// 初期値: cnt[a_i]=1
// 取得: auto p=seg.prod(l,r); 転倒数 = Σ_{u>v} p.inv[u][v]
```

## x ← to[x] + ローリングハッシュ（回文判定つき）

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;

const int K=3;  // 値は 0..K-1
const mint B=1000003;
struct S{mint H[K],R[K],pw;};  // H[v]: x_i=v である位置の重み B^(右からの距離) の和, R は逆向き
struct F{int to[K];};
S op(S a,S b){
    S r; r.pw=a.pw*b.pw;
    for(int v=0;v<K;v++){r.H[v]=a.H[v]*b.pw+b.H[v]; r.R[v]=b.R[v]*a.pw+a.R[v];}
    return r;
}
S e(){S r{}; r.pw=1; return r;}
S mapping(F f,S x){
    S r{}; r.pw=x.pw;
    for(int v=0;v<K;v++){r.H[f.to[v]]+=x.H[v]; r.R[f.to[v]]+=x.R[v];}
    return r;
}
F composition(F f,F g){F h; for(int v=0;v<K;v++) h.to[v]=f.to[g.to[v]]; return h;}
F id(){F h; for(int v=0;v<K;v++) h.to[v]=v; return h;}
// 初期値: H[a_i]=R[a_i]=1, pw=B
// 取得: auto p=seg.prod(l,r); h = Σ (v+1) p.H[v], rh = Σ (v+1) p.R[v], 回文 <=> h==rh
// 文字のシフト (シーザー暗号): to[v]=(v+f)%K
```

## x ← (x + f) mod M + 各値の個数・区間和

```cpp
const int M=3;  // 値は 0..M-1
struct S{long long cnt[M];};
using F=int;  // 加算 f (mod M)
S op(S a,S b){for(int v=0;v<M;v++) a.cnt[v]+=b.cnt[v]; return a;}
S e(){return S{};}
S mapping(F f,S x){
    S r{};
    for(int v=0;v<M;v++) r.cnt[(v+f)%M]=x.cnt[v];
    return r;
}
F composition(F f,F g){return (f+g)%M;}
F id(){return 0;}
// 初期値: cnt[a_i]=1
// 取得: auto p=seg.prod(l,r); 値 v の個数 = p.cnt[v], 和 = Σ v*p.cnt[v]
```

## x ← to[x] + 隣接する値の組 (u, v) の個数

```cpp
const int K=3;  // 値は 0..K-1
struct S{int l,r; long long len,c[K][K];};  // c[u][v]: x_i=u, x_{i+1}=v となる i の個数
struct F{int to[K];};
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    S r; r.l=a.l; r.r=b.r; r.len=a.len+b.len;
    for(int u=0;u<K;u++) for(int v=0;v<K;v++) r.c[u][v]=a.c[u][v]+b.c[u][v];
    r.c[a.r][b.l]++;
    return r;
}
S e(){return S{};}
S mapping(F f,S x){
    if(x.len==0) return x;
    S r{}; r.l=f.to[x.l]; r.r=f.to[x.r]; r.len=x.len;
    for(int u=0;u<K;u++) for(int v=0;v<K;v++) r.c[f.to[u]][f.to[v]]+=x.c[u][v];
    return r;
}
F composition(F f,F g){F h; for(int v=0;v<K;v++) h.to[v]=f.to[g.to[v]]; return h;}
F id(){F h; for(int v=0;v<K;v++) h.to[v]=v; return h;}
// 初期値: l=r=a_i, len=1, c は 0
// 取得: auto p=seg.prod(l,r); (u, v) の個数 = p.c[u][v]
// ランの数 = 1 + Σ_{u!=v} c[u][v]
```

# 10. 状態付きの値

## 状態の反転・状態別の加算 + 状態別の最大値・和・個数

```cpp
const long long INF=1e18;
struct S{long long mx[2],sum[2],cnt[2];};  // [s]: 状態 s の要素について
struct F{bool flip; long long add[2];};  // 状態 s の要素に add[s] を足してから、状態を flip で反転
S op(S a,S b){
    S r;
    for(int s=0;s<2;s++){r.mx[s]=std::max(a.mx[s],b.mx[s]); r.sum[s]=a.sum[s]+b.sum[s]; r.cnt[s]=a.cnt[s]+b.cnt[s];}
    return r;
}
S e(){return {{-INF,-INF},{0,0},{0,0}};}
S mapping(F f,S x){
    S r;
    for(int s=0;s<2;s++){
        int t=s^f.flip;
        r.mx[t]=x.cnt[s]?x.mx[s]+f.add[s]:-INF;
        r.sum[t]=x.sum[s]+f.add[s]*x.cnt[s];
        r.cnt[t]=x.cnt[s];
    }
    return r;
}
F composition(F f,F g){return {g.flip^f.flip,{g.add[0]+f.add[0^g.flip],g.add[1]+f.add[1^g.flip]}};}
F id(){return {false,{0,0}};}
// 初期値: 状態 s, 値 v -> mx[s]=v, sum[s]=v, cnt[s]=1, 他方は {-INF,0,0}
// 取得: auto p=seg.prod(l,r); 状態 s の要素の最大値 = p.mx[s], 和 = p.sum[s], 個数 = p.cnt[s]
// 反転: {true,{0,0}}, 状態 1 の要素だけに v を加算: {false,{0,v}}
```

# 11. 区間ビット演算 (AND / OR / XOR)

## XOR + 区間 XOR 和

```cpp
struct S{long long x; long long len;};
using F=long long;
S op(S a,S b){return {a.x^b.x,a.len+b.len};}
S e(){return {0,0};}
S mapping(F f,S x){return {x.x^((x.len&1)?f:0),x.len};}
F composition(F f,F g){return f^g;}
F id(){return 0;}
// 初期値: {a_i, 1}
// 取得: auto p=seg.prod(l,r); XOR = p.x
```

## AND・OR・代入 + 区間 OR・AND

```cpp
struct S{long long orv; long long andv;};
struct F{long long A; long long O;};  // x -> (x & A) | O
S op(S a,S b){return {a.orv|b.orv,a.andv&b.andv};}
S e(){return {0,-1};}
S mapping(F f,S x){return {(x.orv&f.A)|f.O,(x.andv&f.A)|f.O};}
F composition(F f,F g){return {g.A&f.A,(g.O&f.A)|f.O};}
F id(){return {-1,0};}
// 初期値: {a_i, a_i}
// 取得: auto p=seg.prod(l,r); OR = p.orv, AND = p.andv
// AND v: {v,0}, OR v: {-1,v}, 代入 v: {0,v}
```

## AND・OR・XOR・代入 + 区間和・OR・AND・XOR・popcount

```cpp
const int LOG=30;
struct S{int cnt[LOG]; int len;};  // cnt[k]: k ビット目が 1 の個数
struct F{int A,O,X;};  // x -> ((x & A) | O) ^ X
S op(S a,S b){
    S r; r.len=a.len+b.len;
    for(int k=0;k<LOG;k++) r.cnt[k]=a.cnt[k]+b.cnt[k];
    return r;
}
S e(){return S{};}
S mapping(F f,S x){
    for(int k=0;k<LOG;k++){
        if(!(f.A>>k&1)) x.cnt[k]=0;
        if(f.O>>k&1) x.cnt[k]=x.len;
        if(f.X>>k&1) x.cnt[k]=x.len-x.cnt[k];
    }
    return x;
}
F composition(F f,F g){return {g.A&f.A,(g.O&f.A)|f.O,((g.X&f.A)&~f.O)^f.X};}
F id(){return {-1,0,0};}
// 初期値: cnt[k]=(a_i>>k)&1, len=1
// 取得: auto p=seg.prod(l,r); 和 = Σ p.cnt[k]<<k, OR: p.cnt[k]>0, AND: p.cnt[k]==p.len, XOR: p.cnt[k]&1, popcount = Σ p.cnt[k]
// AND v: {v,0,0}, OR v: {-1,v,0}, XOR v: {-1,0,v}, 代入 v: {0,v,0}
```

## 左シフト (×2^k) + 区間和・最大値・最小値・OR・AND・XOR・GCD・LCM

```cpp
const long long INF=1e18;
struct S{long long sum,mx,mn,orv,andv,x,g,lc,len;};
using F=int;  // 左シフトする量 k
S op(S a,S b){
    if(a.len==0) return b;
    if(b.len==0) return a;
    return {a.sum+b.sum,std::max(a.mx,b.mx),std::min(a.mn,b.mn),a.orv|b.orv,a.andv&b.andv,a.x^b.x,
            std::gcd(a.g,b.g),std::lcm(a.lc,b.lc),a.len+b.len};
}
S e(){return {0,-INF,INF,0,-1,0,0,1,0};}
S mapping(F f,S x){
    if(x.len==0||f==0) return x;
    return {x.sum<<f,x.mx<<f,x.mn<<f,x.orv<<f,x.andv<<f,x.x<<f,x.g<<f,x.lc<<f,x.len};
}
F composition(F f,F g){return f+g;}
F id(){return 0;}
// 初期値: {a_i, a_i, a_i, a_i, a_i, a_i, a_i, a_i, 1}  (a_i >= 0)
// 取得: auto p=seg.prod(l,r); 和 = p.sum, 最大値 = p.mx, 最小値 = p.mn, OR = p.orv, AND = p.andv, XOR = p.x, GCD = p.g, LCM = p.lc
```

# 12. 括弧列

## 反転 + 正しい括弧列判定

```cpp
const long long INF=1e18;
struct S{long long sum,mnpre,mxpre;};  // '(' = +1, ')' = -1 の累積和
using F=bool;
S op(S a,S b){
    return {a.sum+b.sum,
            std::min(a.mnpre,a.sum+b.mnpre),
            std::max(a.mxpre,a.sum+b.mxpre)};
}
S e(){return {0,INF,-INF};}
S mapping(F f,S x){return f?S{-x.sum,-x.mxpre,-x.mnpre}:x;}
F composition(F f,F g){return f^g;}
F id(){return false;}
// 初期値: '(' -> {1,1,1}, ')' -> {-1,-1,-1}
// 取得: auto p=seg.prod(l,r); 正しい括弧列 <=> p.sum==0 && p.mnpre>=0, 最大の深さ = p.mxpre
```

## 反転・代入 + 正しい括弧列判定

```cpp
const long long INF=1e18;
struct S{long long sum,mnpre,mxpre,len;};
struct F{int to[2];};  // 0 = '(', 1 = ')'
S op(S a,S b){
    return {a.sum+b.sum,
            std::min(a.mnpre,a.sum+b.mnpre),
            std::max(a.mxpre,a.sum+b.mxpre),
            a.len+b.len};
}
S e(){return {0,INF,-INF,0};}
S mapping(F f,S x){
    if(x.len==0||(f.to[0]==0&&f.to[1]==1)) return x;
    if(f.to[0]==1&&f.to[1]==0) return {-x.sum,-x.mxpre,-x.mnpre,x.len};
    if(f.to[0]==0) return {x.len,1,x.len,x.len};
    return {-x.len,-x.len,-1,x.len};
}
F composition(F f,F g){return {{f.to[g.to[0]],f.to[g.to[1]]}};}
F id(){return {{0,1}};}
// 初期値: '(' -> {1,1,1,1}, ')' -> {-1,-1,-1,1}
// 取得: auto p=seg.prod(l,r); 正しい括弧列 <=> p.sum==0 && p.mnpre>=0, 最大の深さ = p.mxpre
// 反転: {{1,0}}, '(' を代入: {{0,0}}, ')' を代入: {{1,1}}
```

## 反転・代入 + 対応の取れる括弧のペア数（最長の正しい括弧部分列）

```cpp
struct S{long long c[2],o[2],len;};  // [0]: そのまま, [1]: 反転したとき。c: 余る ')', o: 余る '('
struct F{int to[2];};  // 0 = '(', 1 = ')'
S op(S a,S b){
    S r; r.len=a.len+b.len;
    for(int t=0;t<2;t++){
        long long m=std::min(a.o[t],b.c[t]);
        r.c[t]=a.c[t]+b.c[t]-m;
        r.o[t]=a.o[t]+b.o[t]-m;
    }
    return r;
}
S e(){return {{0,0},{0,0},0};}
S mapping(F f,S x){
    if(f.to[0]==0&&f.to[1]==1) return x;
    if(f.to[0]==1&&f.to[1]==0){std::swap(x.c[0],x.c[1]);std::swap(x.o[0],x.o[1]);return x;}
    if(f.to[0]==0) return {{0,x.len},{x.len,0},x.len};
    return {{x.len,0},{0,x.len},x.len};
}
F composition(F f,F g){return {{f.to[g.to[0]],f.to[g.to[1]]}};}
F id(){return {{0,1}};}
// 初期値: '(' -> {{0,1},{1,0},1}, ')' -> {{1,0},{0,1},1}
// 取得: auto p=seg.prod(l,r); ペア数 = (p.len - p.c[0] - p.o[0]) / 2
// 正しい括弧列にする最小の挿入・削除回数 = p.c[0] + p.o[0], 最小の反転回数 = (p.c[0]+1)/2 + (p.o[0]+1)/2 (長さが偶数のとき)
// 反転: {{1,0}}, '(' を代入: {{0,0}}, ')' を代入: {{1,1}}
```

# 13. 区間行列作用（線形作用の一般化）

## ベクトルの和 + 行列作用 (mod)

```cpp
#include <atcoder/modint>
using mint=atcoder::modint998244353;
const int K=3;
using S=std::array<mint,K>;
using F=std::array<std::array<mint,K>,K>;
S op(S a,S b){for(int i=0;i<K;i++) a[i]+=b[i]; return a;}
S e(){return S{};}
S mapping(F f,S x){
    S r{};
    for(int i=0;i<K;i++) for(int j=0;j<K;j++) r[i]+=f[i][j]*x[j];
    return r;
}
F composition(F f,F g){
    F r{};
    for(int i=0;i<K;i++) for(int k=0;k<K;k++) for(int j=0;j<K;j++) r[i][j]+=f[i][k]*g[k][j];
    return r;
}
F id(){F r{}; for(int i=0;i<K;i++) r[i][i]=1; return r;}
// 例: x = (ΣA, ΣB, len), 初期値: {a_i, b_i, 1}
// A_i += B_i : 単位行列で f[0][1] = 1
// B_i += c   : 単位行列で f[1][2] = c
// A_i *= c   : 単位行列で f[0][0] = c
// A と B の入れ替え: f = {{0,1,0},{1,0,0},{0,0,1}}
// A_i ← B_i (コピー): 単位行列で f[0][0] = 0, f[0][1] = 1
// 点 (A_i, B_i) の回転・拡大・平行移動も f で表せる
// 歴史和 (x = (Σx, Σ過去のxの合計, len)): 時刻を 1 進める: 単位行列で f[1][0] = 1, 加算 c: f[0][2] = c
// 取得: auto p=seg.prod(l,r); Σ (ベクトル) = p
```
