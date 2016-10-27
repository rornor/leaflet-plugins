![graph](http://g.gravizo.com/g?
digraph G {
	graph [bb="0,0,568,426",
		dim=3,
		mode=major,
		overlap=0,
		pack=True,
		prog=neato,
		ratio=.75,
		sep=0.01
	];
	node [label="\N"];
	WikipediaArticle	 [fontname="Helvetica",
		fontsize=8.0,
		height=1.0556,
		label=<<TABLE CELLSPACING="0" CELLPADDING="1" BORDER="0" CELLBORDER="1" ALIGN="LEFT"><TR><TD><FONT POINT-SIZE="10">WikipediaArticle</FONT></TD></TR><TR><TD ALIGN="LEFT">+id : Integer<BR ALIGN="LEFT"/>+movie_id : Integer<BR ALIGN="LEFT"/>+title : String<BR ALIGN="LEFT"/>+valid_from : Date<BR ALIGN="LEFT"/>+valid_to : Date</TD></TR><TR><TD ALIGN="LEFT"></TD></TR></TABLE>>,
		pos="464.54,240",
		shape=plaintext,
		width=1.4444];
	WikipediaPageView	 [fontname="Helvetica",
		fontsize=8.0,
		height=0.93056,
		label=<<TABLE CELLSPACING="0" CELLPADDING="1" BORDER="0" CELLBORDER="1" ALIGN="LEFT"><TR><TD><FONT POINT-SIZE="10">WikipediaPageView</FONT></TD></TR><TR><TD ALIGN="LEFT">+id : Integer<BR ALIGN="LEFT"/>+wiki_article_id : Integer<BR ALIGN="LEFT"/>+date : Date<BR ALIGN="LEFT"/>+views : Integer</TD></TR><TR><TD ALIGN="LEFT"></TD></TR></TABLE>>,
		pos="464.54,83",
		shape=plaintext,
		width=1.7361];
	WikipediaArticle -> WikipediaPageView	 [
		fontname="Helvetica",
		fontsize=7.0,
		head_lp="433.92,120.62",
		headlabel="+pageviews*",
		pos="e,458.92,116.62 458.68,201.87 457.58,179.25 457.5,150.26 458.43,126.68",
		];
	Movie	 [fontname="Helvetica",
		fontsize=8.0,
		height=2.3056,
		label=<<TABLE CELLSPACING="0" CELLPADDING="1" BORDER="0" CELLBORDER="1" ALIGN="LEFT"><TR><TD><FONT POINT-SIZE="10">Movie</FONT></TD></TR><TR><TD ALIGN="LEFT">+id : Integer<BR ALIGN="LEFT"/>+territory_id : Integer<BR ALIGN="LEFT"/>+global_movie_id : Integer<BR ALIGN="LEFT"/>+title : String<BR ALIGN="LEFT"/>+lang : String<BR ALIGN="LEFT"/>+release_date : Date<BR ALIGN="LEFT"/>+genres : ARRAY<BR ALIGN="LEFT"/>+deduced_bom_genre : String<BR ALIGN="LEFT"/>+deduced_production_budget : BigInteger<BR ALIGN="LEFT"/>+deduced_theater : BigInteger<BR ALIGN="LEFT"/>+mpaa : String<BR ALIGN="LEFT"/>+locked_columns : ARRAY<BR ALIGN="LEFT"/>+distributor_us_theater : String</TD></TR><TR><TD ALIGN="LEFT">__str__<BR ALIGN="LEFT"/>__repr__</TD></TR></TABLE>>,
		pos="165.54,83",
		shape=plaintext,
		width=2.7639];
	WikipediaArticle -> Movie	 [
		fontname="Helvetica",
		fontsize=7.0,
		head_lp="279.33,139.73",
		headlabel="+movie",
		pos="e,265.33,135.73 412.46,212 374.42,192.28 321.48,164.84 274.36,140.42",
		];
	WikipediaDailyMetrics	 [fontname="Helvetica",
		fontsize=8.0,
		height=1.0556,
		label=<<TABLE CELLSPACING="0" CELLPADDING="1" BORDER="0" CELLBORDER="1" ALIGN="LEFT"><TR><TD><FONT POINT-SIZE="10">WikipediaDailyMetrics</FONT></TD></TR><TR><TD ALIGN="LEFT">+id : Integer<BR ALIGN="LEFT"/>+movie_id : Integer<BR ALIGN="LEFT"/>+date : Date<BR ALIGN="LEFT"/>+views : Integer<BR ALIGN="LEFT"/>+edits : Integer</TD></TR><TR><TD ALIGN="LEFT"></TD></TR></TABLE>>,
		pos="165.54,240",
		shape=plaintext,
		width=1.7083];
	WikipediaDailyMetrics -> Movie	 [
		fontname="Helvetica",
		fontsize=7.0,
		head_lp="151.54,170.28",
		headlabel="+movie",
		pos="e,165.54,166.28 165.54,201.87 165.54,194 165.54,185.35 165.54,176.44",
		];
	WikipediaPageView -> WikipediaArticle	 [
		fontname="Helvetica",
		fontsize=7.0,
		head_lp="428.4,197.87",
		headlabel="+wikipedia_article 0..1",
		pos="e,470.4,201.87 470.16,116.62 471.4,138.42 471.62,167.46 470.81,191.78",
		];
	WikipediaRevision	 [fontname="Helvetica",
		fontsize=8.0,
		height=1.5556,
		label=<<TABLE CELLSPACING="0" CELLPADDING="1" BORDER="0" CELLBORDER="1" ALIGN="LEFT"><TR><TD><FONT POINT-SIZE="10">WikipediaRevision</FONT></TD></TR><TR><TD ALIGN="LEFT">+id : Integer<BR ALIGN="LEFT"/>+wiki_article_id : Integer<BR ALIGN="LEFT"/>+parent_id : Integer<BR ALIGN="LEFT"/>+rev_id : Integer<BR ALIGN="LEFT"/>+size : Integer<BR ALIGN="LEFT"/>+timestamp : String<BR ALIGN="LEFT"/>+user_name : String<BR ALIGN="LEFT"/>+user_id : String<BR ALIGN="LEFT"/>+comment : String</TD></TR><TR><TD ALIGN="LEFT"></TD></TR></TABLE>>,
		pos="464.54,370",
		shape=plaintext,
		width=1.7361];
	WikipediaRevision -> WikipediaArticle	 [
		fontname="Helvetica",
		fontsize=7.0,
		head_lp="422.54,282.25",
		headlabel="+wikipedia_article 0..1",
		pos="e,464.54,278.25 464.54,313.97 464.54,305.49 464.54,296.8 464.54,288.5",
		];
})
