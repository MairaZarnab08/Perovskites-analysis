
<h1>Exploratory Perovskite Data Analysis using Python as Analytical Tool</h1>
<h2>Description:</h2>
<p>This project involved a comprehensive analysis of molecular data for perovskite materials, with a focus on understanding the relationship between structural and electronic properties, particularly band gap values. The source dataset was retrieved through a reliable API integration with the Materials Studio database, ensuring the credibility and accuracy of the raw data.</p>
<h2>Key Components:</h2>
<ul>
  <li>Importing data from Material Studio using API</li>
  <li>Data Cleaning</li>
  <li>Extracting specific compounds for perovskite analysis</li>
  <li>Calculation of mean band gap across crystal system</li>
  <li>Distribution of band gap values across different materials of O3</li>
  <li>Counting the number of atoms that are frequent in high band gap compounds</li>
  <li>Comparing band gaps of different perovskites</li>
  <li>Correlation matrix for different properties</li>
  <li>Distribution of band gap with respect to density and volume</li>
</ul>
<h2>Utilities Used:</h2>
<ul>
  <li><b>Programming Language:</b> Python</li>
  <li><b>Libraries:</b> Pandas, Matplotlib, Seaborn, Ast, regex, MPRester</li>
</ul>
<h2>Program walk-through:</h2>
<p align="center">
<br/>
<img src="https://media-hosting.imagekit.io/ac6cabdf847a4dec/Screenshot%20(283).png?Expires=1841672887&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=AqWrsmhOuOtPbNblUti~~d-CH3ZJyLBr5xZVZ3e91iX47trEqs1RXS43JHlHChWQJaUMqXgtGGvwI8LPI70mUcE8GRkc7QjpiCsqYlkF9vVkz5IjnZMfO5qWVfqx-GkUSxaODnlT~s88fldcSgl3rEzmQDYCRz~V9qMcXFegxIZU-KFp4RxpQSJpAWTnJ6moXuwhYtKc6PNGGfrEu2pGp2WkzeUGOaLtDMY8Ea3i8JBk07Ed0t7IvXdAHPwTwy0~2XaydO2Nwz0kq9JwrBQnBJXJv0~lvceaeEF7AM45ne7TtZMaVaLiV2vsKx7KOuF8-cPTd-9R8GF9UZ7cym8FoQ__"/>
<img src="https://media-hosting.imagekit.io/eeb98c86cb694995/Screenshot%20(254).png?Expires=1841650373&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=2T3KKVNpn1kRD61SVB-fbe2U-nv2MWilE5LqcJtJcIGviwsk92SP4UB8J2dNCrmV48p6rxFPzi-pVZPReGd3yAOxvxfP2uugrCoRKDVWOjK4lYuKQdQZs4reL4Z2Au-spA~K25PWWqOtjR3DvGQZzp6Mp1rSSwndpvM5XDwFKx~sK6OADGHu39ZgSRjo5XsGs~ZnUxDM-TwHcmBmJAvxAud7DMy-IlW5NHdINhzmhjZEBAaCPkBjr0~cTiLLA--k134r8RSXwNT43gp9y5CqaOS3z4Bw0Ma02yHXdWj-E0QjMCOw-P7NN5Y1WQDFkl-sUaEd9U9Oxzk~Ci-0BSbAOQ__"/>
<br />
<img src="https://media-hosting.imagekit.io/5594067a8db440ca/Screenshot%20(255).png?Expires=1841650513&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=UMzK7tuM6ewbCxhLdUK-9K-TEKS2AMnNnvPQcI3veLR49GTJkljsXLX4B1c2uPgP0vYRkx7~Jb6erJnplW-CrjtjYVx9Y~LYxEjHo49RPxAMbpLDTCmMMKkH1hb3usiGTCnI0seSPUVJPJSim0Tu9ZCItCg6AJG~BnQEzGrPJyt15rsD~QAFobwCVge9nNWv1Ku9U5-odn5WIr5Ht~e6Nf9IsPGsVJGQN5m7Av8A7drgqB-~FjGS-PVf~-remad08ZfHhK4e~ryQBhZ7KFNvCY9sCZWELAy5vYKsg-9ike61Lg3f50ei~pdY7cW5xQ5cszLIAgCUYI61HpM~YCe05g__"/>
<br />
<br />  
<h2>Data Cleaning:</h2> 
<p align="center">
<br />  
<img src="https://media-hosting.imagekit.io/65004fc7f0f74dd5/Screenshot%20(256).png?Expires=1841650680&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=pubaiEp2hbA5FTRZ3ir8XFtxZVYXrmrakJHQE0UD29zlZPkHQ4bzlGNLAuCXgTz1eC7o4y7LVyUChFbq8MXOgLYxBOfLaJDRJRQ0ROcQT80S8e3qIIjAkxU7o446Mwia4EVYaqqQksZYPI8TBsdkW58Bkg9X8LHewDsbLQF6ZL4LFaEfmura6nA4XQiMG0tEBjtjLOHi0gXGEPWdO1cbmyG55UiOqulJhRZ5d~ZUSBSsz9wV0a2uAtpQOR0W~IrERtH4XC471EQ2WSuXOORDgpvAu-zdFNkJDf2OvAtZStFrU68PRvQjljicOl3mRiue7vnqc8hsrXU6UBi8uNCUHw__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/c91d4aef9632464d/Screenshot%20(258).png?Expires=1841650720&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=rti884C6tKt3754SH7MB5WhOweXvbNZK~NJ8JoRKleavEXfbhZebqbeXDclert~H5thgdt9I~8Wg8O~PI4hswE5Gbx9bBUf9Bp68kniC4PVRj0syd4naSyQTEl~p7IiNW0F88eNQsVSSY3qq5oJXh~8jEYWJ1QE51L5JIszNL~wU0stbIlnMvs-hrk7RuO18FfZmAzznS9eOqBtGwY6z6Temsp1I-i6VS5U5vRrbgwcqiV6OcqQ9o8WUq0FAOHHdCML05~urL3FJGboKGvTPwnRSw9~2HO~AbvS7BG-XeOuWZhGfFZGqGEWFObcZo08HTB4pJDGRrkNggRA5IcZJcA__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/a900d4df35c64961/Screenshot%20(259).png?Expires=1841650773&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=GSVHsiTzpFkp6HLwgpdAmpdBJZslku-abtHrlUToEnhtHjBd8si3Yy813mgcz6hTitJdacNPZ-u8XR42502mf49AufQ07kmiF7gG-lbFLj-nlmZs1H-WSXgTkfTqdyn4gUQMcl2ChqQfYzSoLoK0jQ~ZVA3b9LXj6Ef6dPOXwohyVXhXF44p7sppNTHmvMVCk313k-cKBcnaeHXwlvPS3qvUWLhh2x8RKBnKep4UgU0PlZA76EN4RjuNuOn00wKMb8wGt4RK0bbMhWi~57HeQyciCaLP7B2~shUeTBJC5xaojUCntzqY~nr88CgEw68YvtOI-CyiLfWxnXo9udWoJg__"/>
<br />
<br />
<p align="center">
<br />
<img src="https://media-hosting.imagekit.io/ac929f015dba4714/Screenshot%20(260).png?Expires=1841650820&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=c-PT7xpvUY9Kz~U96J3xgZv6sRqXEQVJ2XRkqgM~jCFiqGlsz7~qYnM0fXhp1WSP3onbE~R02rj4eulDOT~Th6MZzCvz-uPh138~EtGfiJUmTNXRavKDNLz4kvssNaTs06uklh4LieK1dOZBltJ9ltSfolt30UQUPxWms3Pr80iMZ24HfSgOL9oONuxiikDJevtfBLbyXUKn2x9QX08OoSB33EOwLLPeN9nZgUyfqU7VfSPDyD2rBMAazOeRLj1bC-uAgKj5acmpg8GIqAWnYdmapziA-aSRJHQGiNGIL4M1GepGgo1f07r0RCFStkbs5qoG2hQXLNCcJr66zvDW4A__"/>
<br />
<br />
<h2>Extracting Values for perovskite analysis:</h2>
<img src="https://media-hosting.imagekit.io/a2bdefcb2d284058/Screenshot%20(261).png?Expires=1841650858&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=GkOBcgaHvZcK2iz4JcclSBxn6kKgyCGSliY29EAaRWLSSZGQ8J7ZurCYLOz4EKuftYe2rRpeXiqojjU7TZCvAzUBdebVaLmw4npOhJ~IKuKhUdK8VKDXQLWaZ7F~exfiiPyBHHmzHB51c6dJyDb2oLcl1cGJpjiO~GpVnnip2ftrjvmmNG9gOGQrRt4mx-Xhe92d9O6S33RGKvC9gQGAxj0v23IKzwivkbs7EoAsMcOaxLcWjZGpCLxP5JT6VjovEj9CiEZ2hpG00pdw6LlndZAsfbJwHm-hxB-IC3iOBjWUdQYbqqFR8rX1DSR7lWY~yTC06HMgPBU0TzcSCipn~Q__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/3590802d3f974534/Screenshot%20(262).png?Expires=1841650879&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=lkbZLZvHPxJ1i4b4X-hfas-KawvGkRSCKltPTfEbp-fzj2KsWN6Z-JUazJkSw~AMx57g6mXP6zvE2ZSHoMNcKOmpVGl6uZM2GKW-vFzmmLNY~BhML1lJ~ot0BwVqkp2NxbYBPpADfVNnmjlYvLHRxM2ww2iY~82acCoOw~5RGS6iEOTvT3qkIFY5skmnmbhfnve0MxZGt8RnuJmo7ZPEYl5x08B1t~JCFswO-5tci~CmCL1V7dEJ2NqaH46Tvj6EPmg4cdV1mXDFHgg8kNQslA~XxAJf0tTj8efzzDQDR1IbBl0E~0QaHl9k9ZY-2-NWgZWxY1ji4XoDtZP5qjaaRw__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/28752dbbb22342e7/Screenshot%20(263).png?Expires=1841650904&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=ZMcWCCfPiNgQvK9UB8b4ziPoew4OVfI7W0bXUBgOLPavdY5vxRlk4Rl9i5Xz6JFUF52dqPKstq~2adVYcTbbE9JCsHhGxUdTu-L~g9vpZ8L8-q-sFIOBoWyTGrDZHyq4ze732FLVqNDjTxzGEbYLVeuNj--M5fBiqgfzNPOr8Ho9QuxUcqUNsl4utJf~XZzNa49ku1~IF~Ne2RmvZmh7t6EpPK5bHXagjkhj6FTRY5P36f9Jo7dbMyWc-9Dfw3TgVrYpoEJCPYvF6K3k2i8IhRqT-D5pNbie9-K2MD4oKUrsm-h5TsFXQBC6gSjT~fe0dWAi-s8me7mF3K6ULMnlRA__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/4ea227932be84746/Screenshot%20(264).png?Expires=1841650927&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=kw40XVq1Gc3dsPb678smNRYCgAw2fxSUMG50fpXHSt1M9c5v15VB2FKtL1m1wcFk1FIp0NVYbGFxoYt3igJ~HtHQq4oWLKPnd5lWal4ziPd-94SFk3~shlbrvtO1cbAA09sE~n4FnIjt57MFIC8jjDLgsqJScDO5VeRrozZfyu~m4EkUsD1ahYRbzp7SL6rxKcD0ecVXbZiMHgbL23sxg7IRemmyou1TDT61kNwBbz0QClAoh-sYJqIk3jKpuVUPiWllAsZICzli44BthJP-ZIu6vkpNeKdeMXqiCUYh8drAkxhX4TL~~ARIwQaJFrdPG3VeCJ9bpM6X0hroGTxTEQ__"/>
<br />
<br />
<h2> Distribution of band gap values: </h2> 
<p align="center">
<br /> 
<img src="https://media-hosting.imagekit.io/7b3bcf4d82f34e70/Screenshot%20(266).png?Expires=1841651002&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=JQeMqlVqDjakPods-Aya0Isil~8MwJ0Ox1l84eC1STrtsa7QU75XsLczuk~VVTqowK1cDqNI0QjrVZOL19e6aymqyGZnkOcGzyuiQURQygS2Qt8c5JqsbPQTfOhxXzD6LybbsTh9ltCiIOdkKwG0aZQHeTmAxDKTUypNxDLrSS3m4PeGhP701yj4VO1SI~oXlLb93sO9tJ~L7h8vzVt07d4gn-z1O9ZZHsBmum1UWB80QQ~DTL3NnUEYw7CFQ7XfqUztw28Czhp~eM4Gqiqm3G2Zl3XVAMOGF1F51wR59Ebrs2TR9ghLn8Y7RBNjGtEYuWICyQJOuldhuSnYUsTYoA__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/9ca8bbb48bf24670/Screenshot%20(267).png?Expires=1841651023&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=UfK6iwCicU8kFmkbGgdrDsIhq-1kN3kq4WIAz9OdhNthkNE7om3fCBOfRpfZjs0zu0j4z666fG6Ie9mA5~0jmJE6cYlfGsQfPvWMvwl-j8~YbRoLe3eeKTGyW-eExBqYREv2svP7KF2xSNNJEiG74x3E3qnDKP7ndz6~zpW~58PuWK8Wr9mbovzwDHgdg2e3qO80e1FGxU~-39lEX5TjN0~bXZDafNbgMgVErCtZ0boc6ZfSAEPLof3BsOld0hrHFxxa10p~HqEL7B~iXz8PbpF5H0Lv7Ke0wUlI0-E~1nu08WBQnvlbUYZtqLGKX9j4dpAlHg~PbdH-PbVv2pvFtg__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/6d7692e29b3f40f0/Screenshot%20(269).png?Expires=1841651053&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=Cw1FeqVDZdRpNMllF1OyoUVw-w0yQ3yfogHza8Kmv88xcPti6Ss5hog~r0Fo9LUB4F8V3SoNPPIy66OiMVQXJRKuR9TmSHKKwf-ngM0~JR4bQAtyzE-HonmN5VZHFXUCNhnDVo6~oM84H4J67qnxLIUc-8ppeQVtVrkYYDlVU5bY7jgiTZ-EUmmbO1VUbzBiz51beku2HLo-nfWj7-Z8GV5-NM60xa1Km0fkbTADZiYNQrczw1lC9-WTIjPCenjldl~akjU~Bfz10cYutA4THd829Ks9v7dmE6ab9j~It~9c0nwl8PUF949rK1KHrKNlJPxFjTZaGjLI8OIrZCY2YQ__"/>
<br />
<br /> 
<p align="center">
<br />
<img src="https://media-hosting.imagekit.io/20252f86a3284e41/Screenshot%20(270).png?Expires=1841651093&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=D-KYPHi2zHIMldeKmh0Fh7vW4Sm5ZpQjJAdwl4goY9Qzyb61hgEzPUXBFvIJzPWewhosY-~MQA8cko3B-XqF~dpG1iIcAXY7Y4J7mI3I1KkF-nvKSYRGR5Cq87XUKqXAClAbgOIdQ-Jhv796d41a8~NOtPDTcczNjE6r0LSLfm3AGNrm6sggCRCjEJx0wRoBc~kqTd-qEtJJl1ULSDkJ5pJkEFnMzhNbycAThnRVrUb3thnetU9AOv02ISdy5dp-kw2vjPEOLICcw3tp1hneXcENvnIPtcoc6r-5OtJQO~91Vpfn-Sx-9LqcvMq0PgFNe3ox7P-CVOc6TwbHSfm2vw__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/ce7e97f67b9148a3/Screenshot%20(271).png?Expires=1841651115&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=Sgp2R9CMudZHpKFXoyW-iOGcP65qgwbnwMV0ILmGj0s-Qeju1yOQjAOifFabYKO4yBahHZPivIMXT7Csv9PR4QHOeST5soPwAHuXwcppDCLc96fMdep4SjYFO2W1Q8IbN6G-~yUzrnltei03n7~gGW-OsNQAovRUSZn7klQ5duDoGQCfyyWS9iyttkysleDex12p9GjBULS8VTxl~3v-TDgXKeen7fxM-Xb3AuAZXxtYluf3DFIZ~yab-ZnFfKjcduTbGorHqatXYHo33XOrImOIqedgBwH9HX2XhrGnBOCpINZZ8maAdkrIOaKvwc-1cm9LRvoFdxmDwRApPxrVUg__"/>
<br />
<br />
<h2>Comparison between band gap of different type of perovskites: </h2>
<br />
<img src="https://media-hosting.imagekit.io/8ebf040dfa1f4f9a/Screenshot%20(273).png?Expires=1841651195&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=IyRXeinj~HE6bZBFh5NoFDuaV1ua67ZjqKGBtsK2Iz98yiA8N77wx9sOYNAkbCikfYO0GmHNRKuoTWbgU5Ca1rKEDAgmmn7~IXSzZjxTH7MbzzOCgf-Nj5J5H7y74EpyQsw~YyvPXYYzLIjsTKLKxpscAjGds-Z7PzTjOom104-T~2SbT9APMouCsSWcjB0hqZyM15vAR5RTZ7CouY3CHC5HeDa2I7aE-PGPbhSxi3W-v3GY1RL-nsRpEBZa07X5V4O0lzFu4hfHGuhSzyIuIpfjzFESPnYDMZAN53MZabYNVBceEfrTM2FYXUUzCW791InGkTh6n438MBdwUszoFg__"/>
<img src="https://media-hosting.imagekit.io/800644b6e40449c7/Screenshot%20(274).png?Expires=1841651214&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=sUWkQ1-wdLpYg0ySBuOFpUGhnGMxhvE15DZgV7TVHp-VXYlok2pwUoYtNPDVtN-6A4o8uypw8UZbvWyWfKQVtrjk7LrVMytS1N650ibdmTNI4sZLUUG7sQbAxgTZegNdh-ij3jAeSfdBk0~ENYnCLS74owfurDRH5Ty5y2vFpuTKbGelxkzVATZK9aaYaoHOg5lhCsl91oe1o8cBvF~mnZvK76VdBwflz0pVcMsYqWkJGQ5NJkVajqfyrf9YiECdavcDjTYrNLK8DC3xXaC2TwDxcWPmteXa11swbjt0abGUfw74bPnTc3ODcMA~CkF9fH1h88~FKbbkuW979QO6tg__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/5be5c7aa88ba41ae/o.png?Expires=1841651965&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=SzopNCkTFLliJerXZqVgEK2ssYMwMdy4WK~fNzUQwT1lQBfPvlIrVaESFt3Z3hEuhg0fvAvv9~uK-7sbS1urrUaHiwqUmT8oFDvO0MI4fWjpQ-~v4mB-7UfNEu8CnVFQr~mlPsmatzWsRUCh7NO6BrhSsyurpdb8tEOI8VPZnQ5y04KVMJboIAzzTWM-YT3-TAjvBjhnET64dL4KhzNYKx4W7b2bWGAX7HIY7cghohAuBgOYR~ajlEFEjWipV99lmp0yiLpft8WiVRpM3zyZRnCE9GvXGCWsHLBHTj-y0nEj73w5B2hjkTmz3Iqba1fOpel~cN2sLYvUdu-tIh3EIw__"/>
<br />
<br />
<h2>Correlation Heat map: </h2>
<img src="https://media-hosting.imagekit.io/e71ccc9a7d044bc4/Screenshot%20(275).png?Expires=1841652479&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=z2vOYxLVXNrO8uk4RdtaFNpmKTNqx5kKSXGBJTIJXPhD6GRBSTufw4RTXvWAyTSv1i2u25fVMDy2sC7H~gWsIShiwO49vYZqW7IaTT6BT1176RPVQhXPry~FJTJv5Cioj5FiCpOD1V-~fV3EgULbaSv9jpEu0SCAkuO4Weyr7BIX2Hg3v0CZiA33y2BuOLN7n2QVv9wswofuevPtxRn4JfZ-rNp2sCvmWdlWRVMssFzsQX9jYmf2311vQrfunoxuI8GDHvf1Zlwr06BQWwTwEkS~1KDmjLGPwJMwDT0Bb8We8XnWBrDDMybgwvEjuCjYBLfQ1gGtaqOF7FrMDn02YQ__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/766ff940064c4f65/Screenshot%20(276).png?Expires=1841652496&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=T5q0PnidRQrjo9gAVAFpYSRNBvYt6ayc8vu9d9PbdsgDIi9bpTXnkfNhfAwBlZrO~etZJ2heHWckYJJ3XTJDFJHQTDbP1LOouui0P7Qc-QzHjAnTOR4~OpxoAqYQmROS2-VpEwat6-ylih~11oVxaCCW8xzkK5q~GHx8IcEnxMbS2sbGJH4VWlC6j7IQJv1NtcM00Z~mEOYv~E-FqpYhtKopBLov5SnbqOwHIoxM1CH0kKI4YqTK24j0MPvEqqAVH0J9APiKHzU5UAr0DTPA8eMrmzq4~Zn6utRLzTo1saInpR3nLbWdm9gmtr1RWpRdrffK1ncN8nGaHY-neHXiag__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/71f338ef394c426f/headmap.png?Expires=1841652787&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=R0xzMM3EpCeG5-zXEauxFt03Z3gfrKO8dirTTpuE2rqp0xMvRu-SQGo5tNDQExDESC72RfI9ICgwgsuLQm65XRtYtT~0Z~nBmNfij-7KTiOjfwWPKVYdvO3g4UGhBsUPgj~ChNAKRUtc4Paaf3pZ02TPLohFv80KbfXLDL8QLLQE2fJRbBrslEkwtzbWwhKvosnfs-~mhKC-5QWiU2xRvqyai4E~Ii2suWdCbsDBP79pZnhI3zs01vXSrLsGBB3umC7oy~CFftNGaEVHoIAK73jwMZ5m48WWHbltvRubQM-808zHGturqw01b2kbnUXP7Qwx3XVODQpCUOevGV8aTg__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/2d0fad2ea85444f1/Screenshot%20(277).png?Expires=1841652612&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=zxLGLIYpAhtDguXN4piKHn~b-~IiGMVBOCpoRwZMqPdvYlNEk072vM-cS8wSsC6F9-zV24AW064hfMtfiO6Rg-lFsUMGciHgG8X5sUiTb9fek1xJu9LhjHVlhid3OGa4jcrD14TBBU3wzraWm6GGZ7D2OyLwQP2l1AVbEvtu0q1HbXi1huSKYhbRDFIr9Ol-S7toPM~7ISgeqUisTjGFvdt0zkd~gEBSO0Rxg5c7efa0Tl~lzpxdz6SqvI4F8SqounuwAzE4XGDfdKp88kdRFZ~mzD7kyQDriAXU5uwvbTRq4rWIytBWAIjMN4xDlyLQK1OmdrTZ5X1i5Xtv-CXKSw__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/b4818b10852a4840/Screenshot%20(278).png?Expires=1841652648&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=mMErul~le5Z4fn6VGRm4pJbZFoVGRbmT87W-1qTL8Tt0S6gfxzRrR2qaZQOTXfJxIrofsO60DQ0z~5mQsatelU0sOYRipdgJ6~5ibaUBScFK3-4B7w9SH1eRzStudABL9fC94K3CyTPSkQoIiL0AbDG8Dnst6xB2DiKC4Q6qQNLUOTePhk3Zoce6UMG6qldiq19SeXs8Qr1xy6DIjNq8hEgIoTG3NoJQt6DmuLJob2dGeZbH44UTURCnHeyg6NlBmLETz90Qztkf4c0awivGZrMqnH-mgngKUCDmdAghSuoFDf9F50FGhoskiT3yXLK67xpK1HWPcdOlTyVKPyzCmA__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/e64809c605a64d3d/Screenshot%20(281).png?Expires=1841652667&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=pwGUjOegTrmB4Ki-N2hM9~BQOnFxY6IUzqx9e8cpzv~AYxdOujMayY2qVDqr0LI5jzh5cNXND3Q5mtkwgA9Ly~pP2CKtAgoxPLdntiXtpRsPH5OnGVWtG4eKvorrXuWwjbs6yaATe1~Escw2TyudbHaMx142W3PLehVTQLd7B3L7L1eHL-W7MqRgv~NSYNJkHqlHGyRK0dJt0XRnftjj~qJe3r4puKWkN5Df57UHuWVeXWubG9sgvlOtoRr7jjAab0BYrtAAkzkUppd5cZKggcrZBxZnetJKSaXF5su3gEZxV-UgrkOstJdTEyNrpXvvtBEh9rPq6iuhLqy9k0mZ6g__"/>
<br />
<br />
<img src="https://media-hosting.imagekit.io/36c4dbd898e94421/Screenshot%20(282).png?Expires=1841676847&Key-Pair-Id=K2ZIVPTIP2VGHC&Signature=xS~wvLm8JHklyKmXcrPmEj3DMDKvSgOLrC9yTeOXURCOLXrNIl4coBWNAbX-yQ~DAD1QYpKX9nN557I8UHEnqvtGWIY997QKw1p7-VhJLZcfwkjdPd2YgA2Ls3auVkJ9Pf7J1z4y~3CAmhcM1SQnOYw6CQwdk5~6EOroJ6rRSgRkk0Z4jNUvMJxLS~-gWwbDykgS4shvTi6XiO96DSlqy6P7jYsemT095MDYmTxDrgf-H2h8rtIMtp2hdDu10ND3eY3xTiR5k0Zxga-Cn5ar1GQ0nq-ON~CEjOBtl7sbz~g4GcIjqulsZ6fDyTzL77FKSb-wSNLRgWY2OMxQQZsgcA__"/>
</ul>
<h2>Project Findings</h2>
<ol>
  <li>Source data was imported by a credible Database called Material Studio using API method</li>
  <li>Data Cleaning involved extracting desired values from the column named symmetry (to get crystal system) and elements (to find out which elements are present in the compound)</li>
  <li>Mean band gap was calculated for every crystal system, and it was found that the Trigonal system shows the highest band gaps</li>
  <li>Out of the data, semi-conductors were isolated in order to perform further analysis. Semi-conductors are the compounds having a band gap higher than 1 eV.</li>
  <li>The distribution of band gaps of these semi-conductors was elaborated by a histogram. The histogram shows the distribution of band gap values, with most values concentrated between 1.2 and 2.2 eV. The blue KDE line indicates a right-skewed distribution, suggesting fewer materials have high band gap values above 3.0 eV.</li>
  <li>The number of atoms which were most frequent in materials having higher band gaps (>2.5) were counted using the Explode attribute of pandas, followed by extracting perovskites of (A = Ba, Sr, Ca & B = Ti, Fe, Ni, Mn, Co, V, Cu, C = O3)</li>
  <li>A stack plot was made to visualize the band gap differences of perovskites (A = Ba, Sr, Ca). Ba compounds show a wide range of band gaps (0 to 2.5 eV) with many low-gap materials. Sr compounds are dominated by near-zero band gaps, with only a few outliers around 1.8 eV. Ca compounds display more variability, with several high-gap materials (up to ~3.3 eV). Overall, Ca compounds tend to exhibit higher band gaps compared to Ba and Sr compounds.</li>
  <li>This correlation matrix shows the linear relationships between four variables:
    <ul>
      <li>Band gap vs energy per atom has a strong negative correlation (-0.73), meaning as energy per atom increases, band gap tends to decrease.</li>
      <li>Band gap vs density (-0.047) and band gap vs volume (0.033) show very weak correlations, indicating little to no linear relationship.</li>
      <li>Density and volume show a slight positive correlation (0.16), while the rest are near-zero, suggesting independence.</li>
    </ul>
  </li>
  <li>Band gap values of different perovskites belonging to different crystal systems were plotted. It was observed that monoclinic, orthorhombic, and cubic crystal systems contain 1, 3, and 3 outliers.</li>
  <li>Scatter plots of band gap vs density and band gap vs volume were plotted.</li>
</ol>




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
