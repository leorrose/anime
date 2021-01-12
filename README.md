<p align="center">
   <img src="https://img.shields.io/badge/-Collage%20Project-informational" />
</p>

# AnimeRs

An anime recommendation system.

The purpose of this project is to research and create an anime recommendation system.

This project was created with **Python (version 3.9.1), surprise, pandas, numpy and more libraries**.

## Project Research

In order to understand the steps and what we did you are welcome to look at [the research jupyter notebook](https://github.com/leorrose/AnimeRS/blob/main/research_notebook.ipynb).

We tested various recommender systems provided by surprise and these are the results we got:

### **User-Based CF**

|FIELD1            |RMSE              |MSE               |MAE               |P@5                |R@5               |F1@5              |P@10               |R@10               |F1@10              |P@15               |R@15               |F1@15              |
|------------------|------------------|------------------|------------------|-------------------|------------------|------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|
|SVD               |1.2466386318320821|1.5541687172779728|0.950649059275635 |0.821792547358859  |0.808167171644359 |0.8149213634198587|0.8202514385582871 |0.8309929909023989 |0.825583949469362  |0.8211466638160235 |0.8337652391649222 |0.8274009774577031 |
|SVDpp             |1.2419986754697163|1.5425765662960005|0.9450240682058786|0.8188678971128791 |0.7896043125358151|0.8039678745549546|0.8152670698321598 |0.8081014340360854 |0.8116670840928523 |0.8148952263938591 |0.8093891685768118 |0.8121295942674633 |
|SlopeOne          |1.4861570936906803|2.2087201120432405|1.1357538191970875|0.7711254526309709 |0.6837134210019202|0.7247915038745656|0.7695408164097652 |0.6966650348950609 |0.7312889080782549 |0.7745419734419228 |0.7013057648417959 |0.7361012749040896 |
|NMF               |2.1645629629270373|4.685525752648781 |1.8700458723769624|0.2816920600486546 |0.14119405854817188|0.1881016258888802|0.2857974991324242 |0.14254297881599048|0.19020809749813983|0.28034197512918746|0.14092628541548033|0.18755996120225144|
|NormalPredictor   |2.1131366070731525|4.465417596127226 |1.6771977769884412|0.7375367312463046 |0.6174220626313723|0.6721390670385622|0.739920385880311  |0.6281192491352906 |0.6794482920849733 |0.7365212868783232 |0.6249930021652182 |0.6761879041065313 |
|KNNBaselineMSD    |1.398410639904407 |1.9555830380571853|1.0669036306056126|0.8171542147591098 |0.7751485069053153|0.7955949747818974|0.8163007742846782 |0.7942681525203055 |0.8051321513697616 |0.8118771257566572 |0.7903858584239758 |0.8009848818709067 |
|KNNBaselineCosine |1.386878661057065 |1.9236409011799906|1.0594412499370167|0.8213979689887809 |0.784533543361471 |0.8025400900390129|0.8163545535545742 |0.7993945680685116 |0.807783132725163  |0.8158383892107871 |0.7992079190989674 |0.8074369434899701 |
|KNNBaselinePearson|1.3445308500081663|1.8078154533494963|1.0233890437557627|0.8259557346454507 |0.8281990254116209|0.8270710550263767|0.8243993866619018 |0.851271467746311  |0.8376190210853552 |0.8221058734399913 |0.8528147820224973 |0.8371786049786873 |
|KNNBaselinePearsonBaseline|1.3616952899328516|1.8542541675921698|1.0384156709120755|0.825437492764036  |0.8245241125371615|0.8249770259766642|0.8231621627433938 |0.8475920311643785 |0.8351967082933334 |0.822986733095186  |0.8474065493728853 |0.8350150557512332 |
|KNNBasicMSD       |1.570226661708983 |2.465623090366103 |1.1971474624994771|0.8124311320861954 |0.7924152038858621|0.8022951900471206|0.8080096162851834 |0.8103188783128166 |0.8091608679006222 |0.8084163159741713 |0.8117116809127282 |0.8100590349801697 |
|KNNBasicCosine    |1.581839141221874 |2.5023280170790505|1.2120829685526158|0.8141367446391025 |0.8046185243353452|0.8093420770200057|0.8096978987086647 |0.8207100773283991 |0.8151603787070405 |0.8107416695599371 |0.8231951103025006 |0.8169167384814318 |
|KNNBasicPearson   |1.5994029168386406|2.558155128783915 |1.2471166570806367|0.8117581540273585 |0.8852442240077742|0.8469085081555134|0.8124881607018233 |0.9248683691654985 |0.8650416377591007 |0.8120686249394726 |0.9252763600323091 |0.8649827110232462 |
|KNNBasicPearsonBaseline|1.6118365967348143|2.598034123999734 |1.2509494202488667|0.8114238388206948 |0.8773810968790097|0.8431121630087256|0.8113745437872941 |0.9127279136565372 |0.8590713949002545 |0.8112168145381808 |0.9158684707572963 |0.860370022257935  |
|KNNWithMeansMSD   |1.376453047227241 |1.894667290359105 |1.0475985960340817|0.7865885917154793 |0.7356529738828108|0.7602675608077976|0.7861160809941485 |0.7546904741711472 |0.7700824793833444 |0.7880956463052174 |0.7583328079565457 |0.7729274050921704 |
|KNNWithMeansCosine|1.3561673714486215|1.8392448162706831|1.0302110753122853|0.7868170989385913 |0.7383283602817778|0.7617972176531568|0.7864747253960043 |0.7576139898176156 |0.7717712985507573 |0.7864292583108007 |0.7579462791383904 |0.7719195333126818 |
|KNNWithMeansPearson|1.4146044455895619|2.001223608355999 |1.0791284426360759|0.7332763404138787 |0.7558542432040236|0.7443936057240416|0.7348916010729349 |0.7882336547052388 |0.7606223266338507 |0.7326515365412436 |0.7867882071401107 |0.7587541225505358 |
|KNNWithMeansPearsonBaseline|1.4224426318514414|2.023367706554281 |1.0853174245214858|0.7363541324899715 |0.7519017437297745|0.7440450086421799|0.7394133375149993 |0.7817954082195213 |0.7600109211383559 |0.7389174718046624 |0.7833449643030551 |0.7604816730644768 |
|KNNWithZscoremsd  |1.3788847277688883|1.9013516752608104|1.0375657830050327|0.7921137744554245 |0.7449251214848664|0.7677921857833014|0.7883159578134012 |0.7619380637345282 |0.7748966483925355 |0.7905639635792684 |0.7632982633959184 |0.7766838494996915 |
|KNNWithZscoreCosine|1.352955517222676 |1.8305378661693155|1.0190715209106491|0.7946934955949703 |0.7509185907514219|0.772185274711921 |0.791687924868308  |0.7701273671846678 |0.7807570910473473 |0.7924395119312745 |0.7711690177658201 |0.7816573713920851 |
|KNNWithZscorePearson|1.4098987205271505|1.9878695963100115|1.0726010605731058|0.7374811976478353 |0.7585981809304221|0.7478885789975193|0.7366826984480097 |0.7878881304442884 |0.76142295116784   |0.7379844380474031 |0.7906789186941766 |0.7634223713777277 |
|KNNWithZscorePearsonBaseline|1.4228844831131178|2.0247620146889576|1.0821061690189422|0.7405915063529038 |0.7555352981583681|0.7479852870872525|0.7381589224019051 |0.7821479671304233 |0.7595145685006843 |0.741012069427383  |0.7859562669903765 |0.7628183284143244 |
|BaselineOnly      |1.2697012667398724|1.6122320696174615|0.9706569670311722|0.8316958274575785 |0.8497705980038063|0.8406298156194699|0.8277099915973795 |0.8740569539130549 |0.8502486766687344 |0.8291474330794177 |0.8775098014798093 |0.8526399924974705 |
|CoClustering      |1.3119423773901975|1.721237844144515 |1.0056872223575495|0.7875553740390717 |0.7334627225108244|0.7595422081721466|0.7851123516262807 |0.7504443552865302 |0.7673850086073116 |0.7865566256587904 |0.7499012241636025 |0.7677822075326837 |

### **Item-Based CF**

|FIELD1            |RMSE              |MSE               |MAE               |P@5                |R@5               |F1@5              |P@10               |R@10               |F1@10              |P@15               |R@15               |F1@15              |
|------------------|------------------|------------------|------------------|-------------------|------------------|------------------|-------------------|-------------------|-------------------|-------------------|-------------------|-------------------|
|KNNBaselineMSD    |1.366114451914405 |1.8662905047067233|1.0257180408478177|0.7911738379366676 |0.7479011157196619|0.7689264649192715|0.7932282044303103 |0.7726453129628611 |0.782799873244865  |0.7906179767031234 |0.7716868301478375 |0.7810342036265258 |
|KNNBaselineCosine |1.3397746389803062|1.7950521899277543|1.0097669586993985|0.794138035661082  |0.7546255412856192|0.7738750848667941|0.7911257697459891 |0.7752056746618489 |0.7830821348612798 |0.7916984962993456 |0.778282711811469  |0.7849316140634988 |
|KNNBaselinePearson|1.3758228627380191|1.8929320360234236|1.0384445362185366|0.8132247576673691 |0.7934769400866921|0.8032265837483223|0.8108722547278573 |0.8166140099149976 |0.8137310512850953 |0.8086616513336364 |0.8139115408103039 |0.8112759912577345 |
|KNNBaselinePearsonBaseline|1.386860635388977 |1.9233982715905313|1.046915727726262 |0.8112177583992247 |0.7874842924836998|0.7991708171015098|0.8088514391469219 |0.8099789657775173 |0.8094123689997144 |0.8080195476710011 |0.8088802968932496 |0.8084494386625802 |
|KNNBasicMSD       |1.5191509842089816|2.3078984808159335|1.1412651801346463|0.7793433889853508 |0.7754117231052828|0.7773687037854964|0.777907562105646  |0.8030328664694979 |0.7902685913298021 |0.7773839703402249 |0.80362004143658   |0.7902809879917424 |
|KNNBasicCosine    |1.5134314656282049|2.290576422979273 |1.1397030621147017|0.7762801739094788 |0.7841397632377504|0.7801870414483421|0.7759986581933109 |0.8145435330097224 |0.7948018305129685 |0.7732959133553675 |0.8124149618519209 |0.7923727314009733 |
|KNNBasicPearson   |1.5990157401258698|2.5569075530003356|1.2199980848819532|0.8023331017173154 |0.851085663209739 |0.8259885664561842|0.8009415053660452 |0.8850575713925745 |0.8409000483868375 |0.8023692587754983 |0.8872280120293015 |0.8426665197581087 |
|KNNBasicPearsonBaseline|1.5973250474715415|2.551466349317195 |1.2153278186596963|0.7995458743748439 |0.838214207332444 |0.8184217897406274|0.7984467434115674 |0.8712288806584689 |0.8332506736072359 |0.7989812221907979 |0.8723801403450974 |0.8340664847718854 |
|KNNWithMeansMSD   |1.380347012905624 |1.9054472065287456|1.0405027798249855|0.7955981611089108 |0.7322596738904392|0.76261327000769  |0.7942880637489266 |0.7504615010419483 |0.7717492140055853 |0.7931249973563246 |0.7495914461847579 |0.7707412926465141 |
|KNNWithMeansCosine|1.3594823838270245|1.848220424925835 |1.0237033415064871|0.7939217346487165 |0.7339986797423164|0.7627837739418555|0.7969194219707465 |0.7556374574069008 |0.7757293553417887 |0.7952090090469575 |0.756577327821164  |0.7754092842542168 |
|KNNWithMeansPearson|1.4657123912419707|2.148362961025515 |1.1143662829060104|0.8094619961492207 |0.7645702427018006|0.7863739291490991|0.8069140431680175 |0.7817931565415921 |0.7941517595038096 |0.8066891604571055 |0.7831192898349129 |0.7947255274658315 |
|KNNWithMeansPearsonBaseline|1.4714654963505   |2.1652715050911544|1.1159821063439488|0.8046454807449989 |0.7536467103000125|0.7783067073893994|0.808045623453788  |0.7772407764552491 |0.7923427572339874 |0.8047599828915931 |0.775829065773746  |0.7900270966188045 |
|KNNWithZscoreMSD  |1.3864107891660076|1.9222261325140333|1.0434072591502743|0.7988502579149921 |0.7353745582614113|0.7657971379550664|0.7998479030705653 |0.7576271392441782 |0.7781605035271177 |0.7985407981113094 |0.7565247315134348 |0.7769625803765955 |
|KNNWithZscoreCosine|1.363706217881358 |1.8597661579971827|1.026363650331644 |0.8008319650322925 |0.741780819442555 |0.770173023673313 |0.8003679684938072 |0.7628590860032153 |0.7811587045904054 |0.7997159271949327 |0.7615371597800603 |0.7801574466707192 |
|KNNWithZscorePearson|1.470187148489288 |2.1614606542538524|1.1178063051120215|0.8082858259995653 |0.7654649706673161|0.7862886986048343|0.8095214784355148 |0.7847982393158663 |0.7969660351420036 |0.8086023907009723 |0.7856409630683181 |0.7969547888513718 |
|KNNWithZscorePearsonBaseline|1.4712769087180013|2.164661476220339 |1.1167613433425654|0.8081957303898509 |0.7637862095580561|0.7853608757943151|0.8064547414106873 |0.7786464701717015 |0.7923042075702783 |0.8063728267599609 |0.7794109575176488 |0.7926612652211737 |

## Project Setup and Run

1. Clone this repository.
2. Open cmd/shell/terminal and go to project folder: `cd AnimeRS`
3. Install project dependencies: `pip install -r requirements.txt`
4. Run the streamlit app: `streamlit run .\app\anime_app.py`
5. Enjoy the application.

Please let me know if you find bugs or something that needs to be fixed.

Hope you enjoy it.
