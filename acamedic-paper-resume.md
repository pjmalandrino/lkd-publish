# Historique des Publications


## 03 / 06 / 2025
TODO

## 27 / 05 / 2025

💡 𝐂𝐨𝐦𝐦𝐞𝐧𝐭 𝐝𝐢𝐦𝐞𝐧𝐬𝐢𝐨𝐧𝐧𝐞𝐫, 𝐨𝐩𝐭𝐢𝐦𝐢𝐬𝐞𝐫 𝐞𝐭 𝐛𝐞𝐧𝐜𝐡𝐦𝐚𝐫𝐤𝐞𝐫 𝐥𝐞𝐬 𝐢𝐧𝐟𝐫𝐚𝐬𝐭𝐫𝐮𝐜𝐭𝐮𝐫𝐞𝐬 𝐪𝐮𝐢 𝐬𝐞𝐫𝐯𝐞𝐧𝐭 𝐯𝐨𝐬 𝐋𝐋𝐌 ?

La plupart des benchmarks utilisés jusqu’ici pour évaluer le serving des LLM reposent sur des charges de travail artificielles, très éloignées de la réalité. Pourtant, pour bien dimensionner et optimiser les infrastructures (GPU, cloud, orchestration…), 𝒊𝒍 𝒆𝒔𝒕 𝒄𝒓𝒖𝒄𝒊𝒂𝒍 𝒅𝒆 𝒄𝒐𝒎𝒑𝒓𝒆𝒏𝒅𝒓𝒆 𝒍𝒆𝒔 𝒖𝒔𝒂𝒈𝒆𝒔 𝒓𝒆́𝒆𝒍𝒔 : pics de charge, diversité des requêtes, comportements clients…

🔍 𝑳𝒆 𝒑𝒂𝒑𝒊𝒆𝒓 𝑺𝒆𝒓𝒗𝒆𝑮𝒆𝒏 (𝒂𝒓𝑿𝒊𝒗:2505.09999) 𝒂𝒑𝒑𝒐𝒓𝒕𝒆 𝒅𝒆𝒔 𝒓𝒆́𝒑𝒐𝒏𝒔𝒆𝒔 𝒄𝒐𝒏𝒄𝒓𝒆̀𝒕𝒆𝒔.
Les auteurs ont analysé plusieurs milliards de requêtes issues de véritables applications en production, couvrant des modèles variés (texte, multimodal, reasoning). Leur objectif : proposer des workloads réalistes pour mieux évaluer les performances des LLMs et guider le design des infrastructures.

𝑪𝒆 𝒒𝒖’𝒊𝒍𝒔 𝒐𝒃𝒔𝒆𝒓𝒗𝒆𝒏𝒕 :
📊 𝐕𝐚𝐫𝐢𝐚𝐛𝐢𝐥𝐢𝐭𝐞́ 𝐞𝐱𝐭𝐫𝐞̂𝐦𝐞 𝐝𝐞𝐬 𝐰𝐨𝐫𝐤𝐥𝐨𝐚𝐝𝐬 𝐦𝐮𝐥𝐭𝐢𝐦𝐨𝐝𝐚𝐮𝐱
Les requêtes impliquant texte, image, audio ou vidéo sont très hétérogènes en longueur et en coût. La phase de prétraitement (ex : encoder une image) peut devenir un vrai goulet d’étranglement.

⚡ 𝐏𝐢𝐜𝐬 𝐝𝐞 𝐜𝐡𝐚𝐫𝐠𝐞 𝐬𝐨𝐮𝐝𝐚𝐢𝐧𝐬 (𝐛𝐮𝐫𝐬𝐭𝐢𝐧𝐞𝐬𝐬)
Les arrivées de requêtes ne sont pas régulières, mais marquées par des pics imprévisibles, souvent liés à quelques gros clients ou à des évènements ponctuels.

🧠 𝐇𝐞́𝐭𝐞́𝐫𝐨𝐠𝐞́𝐧𝐞́𝐢𝐭𝐞́ 𝐝𝐞𝐬 𝐮𝐬𝐚𝐠𝐞𝐬 𝐫𝐞𝐚𝐬𝐨𝐧𝐢𝐧𝐠
Les conversations complexes (avec plusieurs échanges successifs) présentent des profils très variés : certaines sont très courtes, d’autres beaucoup plus longues, ce qui impose des exigences particulières en gestion de mémoire et de contexte pour les serveurs LLM.

𝐏𝐨𝐮𝐫𝐪𝐮𝐨𝐢 𝐜’𝐞𝐬𝐭 𝐢𝐦𝐩𝐨𝐫𝐭𝐚𝐧𝐭 ?
Les benchmarks traditionnels sous-estiment la complexité réelle du serving LLM. Utiliser des workloads réalistes, comme ceux proposés par ServeGen, permet d’anticiper les besoins d’infrastructure, d’identifier les vrais goulets d’étranglement, et de tester les optimisations dans des conditions proches de la production.
💬 𝑄𝑢𝑒𝑙 𝑠𝑢𝑗𝑒𝑡 𝐼𝐴 𝑜𝑢 𝐿𝐿𝑀 𝑎𝑖𝑚𝑒𝑟𝑖𝑒𝑧-𝑣𝑜𝑢𝑠 𝑞𝑢𝑒 𝑗𝑒 𝑑𝑒́𝑐𝑟𝑦𝑝𝑡𝑒 𝑙𝑎 𝑠𝑒𝑚𝑎𝑖𝑛𝑒 𝑝𝑟𝑜𝑐ℎ𝑎𝑖𝑛𝑒 ? 𝐷𝑖𝑡𝑒𝑠-𝑚𝑜𝑖 𝑒𝑛 𝑐𝑜𝑚𝑚𝑒𝑛𝑡𝑎𝑖𝑟𝑒 !
𝑉𝑜𝑠 𝑖𝑑𝑒́𝑒𝑠 𝑚’𝑎𝑖𝑑𝑒𝑟𝑜𝑛𝑡 𝑎̀ 𝑐ℎ𝑜𝑖𝑠𝑖𝑟 👀​

Le papier - ServeGen: Workload Characterization and Generation of Large Language Model Serving in Production


## 20 / 05 / 2025
𝗟𝗮 𝗰𝗼𝗻𝗰𝗲𝗽𝘁𝗶𝗼𝗻 𝗱’𝘂𝗻 𝘀𝘆𝘀𝘁𝗲̀𝗺𝗲 𝗱’𝗜𝗔 𝗽𝗼𝘀𝗲 𝘁𝗼𝘂𝗷𝗼𝘂𝗿𝘀 𝗹𝗮 𝗾𝘂𝗲𝘀𝘁𝗶𝗼𝗻 𝗱𝘂 𝗰𝗵𝗼𝗶𝘅 𝗱𝘂 𝗺𝗼𝗱𝗲̀𝗹𝗲 : 𝗾𝘂𝗲𝗹𝗹𝗲 𝗮𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲 🏗️, 𝗾𝘂𝗲𝗹𝗹𝗲 𝘁𝗮𝗶𝗹𝗹𝗲 📏 ?

Même avec une bonne stratégie de tests, le premier choix reste souvent incertain.

Le papier "WorldPM: Scaling Human Preference Modeling" (👇 lien en commentaire👇) publié par les équipes de Qwen apporte des éléments concrets pour éclairer cette phase.
Les auteurs analysent comment la taille du modèle et le volume de données d'entraînement influencent la capacité des IA à modéliser les préférences humaines.

𝗘𝘁 𝘀𝘂𝗿𝘁𝗼𝘂𝘁, 𝗶𝗹𝘀 𝗺𝗼𝗻𝘁𝗿𝗲𝗻𝘁 𝗾𝘂𝗲 𝗰𝗲𝘁 𝗶𝗺𝗽𝗮𝗰𝘁 𝗱𝗲́𝗽𝗲𝗻𝗱 𝗳𝗼𝗿𝘁𝗲𝗺𝗲𝗻𝘁 𝗱𝘂 𝘁𝘆𝗽𝗲 𝗱𝗲 𝘁𝗮̂𝗰𝗵𝗲𝘀 𝘃𝗶𝘀𝗲́𝗲𝘀 !

Ce genre d’étude est précieuse : en ayant bien défini ses cas d’usage, il devient plus facile de faire des choix techniques adaptés 🎯

𝑁𝐵 : 𝐼𝑙 𝑓𝑎𝑢𝑡 𝑏𝑖𝑒𝑛 𝑒𝑛𝑡𝑒𝑛𝑑𝑢 𝑡𝑜𝑢𝑗𝑜𝑢𝑟𝑠 𝑡𝑒𝑛𝑖𝑟 𝑐𝑜𝑚𝑝𝑡𝑒 𝑎̀ 𝑙𝑎 𝑓𝑜𝑖𝑠 𝑑𝑒𝑠 𝑝𝑒𝑟𝑓𝑜𝑟𝑚𝑎𝑛𝑐𝑒𝑠 𝑎𝑡𝑡𝑒𝑛𝑑𝑢𝑒𝑠 𝑒𝑡 𝑑𝑒𝑠 𝑐𝑜𝑛𝑡𝑟𝑎𝑖𝑛𝑡𝑒𝑠 𝑑’𝑖𝑛𝑓𝑟𝑎𝑠𝑡𝑟𝑢𝑐𝑡𝑢𝑟𝑒 ⚖️.

Le papier  - WorldPM: Scaling Human Preference Modeling
