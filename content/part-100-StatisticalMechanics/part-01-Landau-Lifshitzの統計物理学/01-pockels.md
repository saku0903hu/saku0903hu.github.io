# Pockels効果

この章は[@Miroshnichenko2015Quantum]を参考にした。

Pockels効果を持つ媒質(電気光学結晶LiNbO$_3$など)に外部から電圧を加えると、電場の1次で結晶の屈折率が変わる。
光子はその屈折率の中を進む。 1光子反応である。
電場$E$がかかっているときのPockels効果のHamiltonianは $$\begin{align}
\hat{H}_\text{Pockels} =\omega \hat{a}^\dagger\hat{a}+\frac{1}{2} \boldsymbol{E} \cdot \boldsymbol{D} + \alpha \hat{a}^\dagger \hat{a} E \to  \omega \hat{a}^\dagger \hat{a} + \Omega \hat{b}^\dagger \hat{b} + \alpha \hat{a}^\dagger \hat{a} (\hat{b}^\dagger + \hat{b})
\end{align}$$ となる。
ここで、$\hat{a},\hat{a}^\dagger$は光子の生成消滅演算子、$\hat{b},\hat{b}^\dagger$はマイクロ波の生成消滅演算子である。
第3項がPockels効果による光子とマイクロ波である電場の相互作用を表しており、$\alpha$は相互作用の結合定数である。

我々がPockels効果を用いる時は、相互作用項のみを扱い、電場の扱い方は量子的か古典的かを適宜考える。
