 Hi Im Arman Ebtekari:wave:
- I love making games and building sites:smiley:
- I want to be a web developer and game maker in the future:cowboy_hat_face:	
- my gmail armanebtekari@gmail.com:wink:
- Follow me🙏
<!--
**ArmanEbtekari/ArmanEbtekari** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
use IgraalOSL\StatsTable\StatsTableBuilder;

$data = [
    '2014-01-01' => ['hits' => 32500],
    '2014-01-02' => ['hits' => 48650],
];

$statsTableBuilder = new StatsTableBuilder(
    $data,
    ['hits' => 'Number of hits']
);
$statsTableBuilder->addIndexesAsColumn('date', 'Date');

$statsTable = $statsTableBuilder->build();

use IgraalOSL\StatsTable\Dumper\Excel\ExcelDumper;

$excelDumper = new ExcelDumper();
$excelContents = $excelDumper->dump($statsTable);

header('Content-type: application/vnd.ms-excel');
echo $excelContents


Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
