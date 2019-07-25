---


---

<hr>
<hr>
<hr>
<hr>
<h1 id="scnc">sCNC</h1>
<h2 id="proč-a-a-jak-to-vzniklo">Proč a a jak to vzniklo</h2>
<ul>
<li>
<p>Potřeba vyrobit levný a jednoduchý stoj, snadno vyrobitelný v prostředí <a href="https://prusalab.cz/">PrůšaLabu</a> nebo domácí dílny</p>
</li>
<li>
<p>Cvičební stroj pro členy  <a href="https://prusalab.cz/">PrůšaLabu</a></p>
</li>
<li>
<p>Komunitní projekt + OpenSource projekt</p>
</li>
<li>
<p>Ovládaní stoje jako téma pro další plánované workshopy</p>
</li>
</ul>
<h2 id="aktuální-stav--červenec-2019">Aktuální stav / Červenec 2019</h2>
<p>Vzhledem ke snadné dostupnosti hliníkových profilů a krokových motorů, byl jako vzor vybrán projekt Dremel CNC + ovládací software GRBL <em>(Arduino Uno + CNC Shield V.3)</em> s následujícími modifikacemi:</p>
<ul>
<li>
<p>Vodicí tyče 8mm na 12mm = zvýšena tuhost a přesnost stroje</p>
</li>
<li>
<p>Předepnuté matice na trapézovém šroubu</p>
</li>
<li>
<p>Modifikované díly z plastu (drobné změny v uchyceni koncových spínačů, vložené matice pro lepší uchycení, apod.)</p>
</li>
</ul>
<h2 id="dokumentace">Dokumentace</h2>
<h3 id="mechanika-hardware">Mechanika (Hardware)</h3>
<ul>
<li>
<p>Hliníkový profil 2020</p>
<ul>
<li>délka Xmm x 4 (osa X)</li>
<li>délka Ymm x 2 (osa Y)</li>
</ul>
</li>
<li>
<p>Motory NEMA 17</p>
</li>
<li>
<p>Spojka Motor - vodící tyč x mm</p>
</li>
<li>
<p>Vodící tyče 12mm:</p>
<ul>
<li>délka Xmm x 2 (osa X)</li>
<li>délka Ymm x 2 (osa Y)</li>
<li>délka Zmm x 2 (osa Z)</li>
</ul>
</li>
<li>
<p>Linearní ložisko 12mm x 8</p>
</li>
<li>
<p>Trapézový šroub</p>
<ul>
<li>délka Xmm x 2 (osa X)</li>
<li>délka Ymm x 1 (osa Y)</li>
<li>délka Zmm x 1 (osa Z)</li>
</ul>
</li>
<li>
<p>Vodící matice 2ks (osa X)</p>
</li>
<li>
<p>Vodící matice s pružinou 2ks (osa Y)</p>
</li>
<li>
<p>Spojovací materiál</p>
<ol>
<li>šrouby</li>
</ol>
<ul>
<li>Imbus s válcovou hlavou</li>
<li>Uchycení motorů</li>
<li>Uchycení vodící matice</li>
<li>Imbus s čočkovou hlavou</li>
<li>Uchycení držáku motorů</li>
</ul>
<ol start="2">
<li>matice</li>
</ol>
<ul>
<li>4 hraná matice</li>
<li>6 hranná samojístící</li>
<li>Matice do profilu</li>
</ul>
</li>
<li>
<p>Pracovní deska MDF (Xmm x Ymm x Zmm)</p>
</li>
</ul>
<h3 id="software">Software</h3>
<ul>
<li>
<p>Controller: <a href="https://github.com/gnea/grbl/releases">GRBL v1.1f 20170801</a></p>
</li>
<li>
<p>Ovládací SW:  <a href="https://github.com/vlachoudis/bCNC/wiki">bCNC</a></p>
</li>
</ul>
<h3 id="elektronika">Elektronika</h3>
<ul>
<li>
<p>Dremel 3000</p>
</li>
<li>
<p>Arduino UNO</p>
</li>
<li>
<p>CNC Sheild v3</p>
</li>
<li>
<p>Řadiče krokových motorů x 4 DRV8825</p>
</li>
<li>
<p>Koncové spínače x 3</p>
</li>
<li>
<p>Napájecí zdroj 12V / 5A</p>
</li>
</ul>
<h3 id="konfigurace-kroků">Konfigurace kroků</h3>
<h3 id="konfigurace-napájení-motorů">Konfigurace napájení motorů</h3>
<p>Pro každou osu nastaveno 1.2 A viz <a href="https://www.youtube.com/watch?v=AVlee67TQxs">https://www.youtube.com/watch?v=AVlee67TQxs</a></p>
<h2 id="konfigurace-grbl">Konfigurace GRBL</h2>
<pre><code>$0=10
</code></pre><p>$1=255</p>
<p>$2=0</p>
<p>$3=0</p>
<p>$4=0</p>
<p>$5=0</p>
<p>$6=0</p>
<p>$10=1</p>
<p>$11=0.010</p>
<p>$12=0.002</p>
<p>$13=0</p>
<p>$20=0</p>
<p>$21=1</p>
<p>$22=1</p>
<p>$23=0</p>
<p>$24=500.000</p>
<p>$25=1000.000</p>
<p>$26=250</p>
<p>$27=3.000</p>
<p>$30=1000</p>
<p>$31=0</p>
<p>$32=0</p>
<p>$100=800.000</p>
<p>$101=800.000</p>
<p>$102=800.000</p>
<p>$110=2000.000</p>
<p>$111=2000.000</p>
<p>$112=2000.000</p>
<p>$120=100.000</p>
<p>$121=100.000</p>
<p>$122=100.000</p>
<p>$130=300.000</p>
<p>$131=500.000</p>
<p>$132=60.000<br>
</p>
<h2 id="stack">Stack</h2>
<p><a href="https://scncworkspace.slack.com">scncworkspace.slack.com</a></p>
<h2 id="budoucnost">Budoucnost</h2>
<ul>
<li>Stavba <em>verze2.</em> ve které aplikujeme návrhy na vylepšení, které vznikly během pravidelných setkání každou středu v <a href="https://prusalab.cz/">PrůšaLabu</a></li>
</ul>

