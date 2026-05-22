# NOS-reductase-domain-in-complex-with-ligands

This repository stores Alphafold 3 models of NOS reductase domain (UniProt entry P29474 756-1002) in complex with ligands: FADH2, FMN, BH4 and GSSSG. The models were used in supplementary figure SXX of article:

    Mammals produce cyclo-octasulfur to suppress lipid peroxidation and ferroptosis

    By: Uladzimir Barayeu, Seiryo Ogata, Tsuyoshi Takata, Minkyung Jung, Tetsuro Matsunaga, Mike Lange, Masanobu Morita,
    Yuka Unno, Saber Boushehri, Paulius Greicius, Tomoaki Ida, Akira Nishimura, Lorenzo Catti, Yuexuan Pan, Tianli Zhang,
    Takayuki Shimizu, Ryo Ushioda, Takakazu Nakabayashi, Seji Asamitsu, Kazuki Fusegawa, Takashi Suzuki, Takanori Ishida,
    Naoko Tanda, Yasuo Watanabe, Ryo Yamaguchi, Shintaro Noguchi, Eikan Mishima, Fumiko Yano, Mieko Arisawa,
    Albert van der Vliet, Dennis Stuehr, Ning Xia, Huige Li, Bernd Moosmann, Frauke Gräter, Camilo Aponte-Santamaría,
    James A. Olzmann, Marcus Conrad, Tobias P. Dick, Hozumi Motohashi, Michito Yoshizawa, Takaaki Akaike

To identify hypothetical conformations that would enable electron transfer between FADH2 and GSSSG we predicted RedD domain in complex with FMN, FADH2, GSSSG and BH4 in AlphaFold 3 using 100 seeds and sampling 5 conformations per seed. See **ENOS.json** file for AF3 input to generate these models.

Since global AF3 confidence metrics might obscure local issues with the model, we focused on predicted alignment error (PAE) between central sulfur atom on glutathionine and C atom of the methyl group which is part of the FADH2 isoalloxazine ring. We extracted top 5 models with lowest PAE between these two atoms. Among the resulting conformations, PAE ranged between 5 A and 5.1 A, ipTM score - between 0.88 and 0.91 and pTM - between 0.89 and 0.90. The AF3 output of these 5 models is uploaded in folder **best_pae**. Figure SXX panels A and B show the model stored in `/best_pae/enos_seed-17_sample-4_model.cif`.

Figure SXX panel D shows an AF3 model where the cofactors were too far for direct electorn transfer. The full complex displayed in this model can be found in `/indirect/enos_seed-17_sample-0_model.cif`.
