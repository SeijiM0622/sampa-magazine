     1	<!DOCTYPE html>
     2	<html lang="ja">
     3	<head>
     4	    <meta charset="UTF-8">
     5	    <meta name="viewport" content="width=device-width, initial-scale=1.0">
     6	    <title>SAMPA - サンパウロ×日本 ウェブマガジン</title>
     7	    <meta name="description" content="サンパウロ在住日本人・日系人向けの生活情報ウェブマガジン。グルメ、ライフスタイル、ビジネス、カルチャー情報を毎日更新。">
     8	    
     9	    <!-- Google Fonts -->
    10	    <link rel="preconnect" href="https://fonts.googleapis.com">
    11	    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    12	    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;500;600;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    13	    
    14	    <!-- Font Awesome -->
    15	    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    16	    
    17	    <style>
    18	        /* ===== CSS Reset & Base ===== */
    19	        * {
    20	            margin: 0;
    21	            padding: 0;
    22	            box-sizing: border-box;
    23	        }
    24	        
    25	        :root {
    26	            --brazil-green: #009c3b;
    27	            --brazil-yellow: #ffdf00;
    28	            --brazil-blue: #002776;
    29	            --white: #FFFFFF;
    30	            --text-dark: #1a1a1a;
    31	            --text-gray: #555555;
    32	            --border-light: #e0e0e0;
    33	            --bg-light: #f8f9fa;
    34	            --shadow: 0 2px 8px rgba(0,0,0,0.1);
    35	        }
    36	        
    37	        body {
    38	            font-family: 'Noto Sans JP', 'Roboto', sans-serif;
    39	            color: var(--text-dark);
    40	            background-color: var(--white);
    41	            line-height: 1.7;
    42	            overflow-x: hidden;
    43	        }
    44	        
    45	        img {
    46	            max-width: 100%;
    47	            height: auto;
    48	            display: block;
    49	        }
    50	        
    51	        a {
    52	            text-decoration: none;
    53	            color: inherit;
    54	            transition: all 0.3s ease;
    55	        }
    56	        
    57	        ul {
    58	            list-style: none;
    59	        }
    60	        
    61	        /* ===== Top News Bar ===== */
    62	        .top-bar {
    63	            background: linear-gradient(90deg, var(--brazil-green) 0%, var(--brazil-blue) 100%);
    64	            color: var(--white);
    65	            padding: 8px 0;
    66	            font-size: 0.85rem;
    67	            text-align: center;
    68	            overflow: hidden;
    69	        }
    70	        
    71	        .top-bar-content {
    72	            display: inline-block;
    73	            white-space: nowrap;
    74	            animation: scroll-left 30s linear infinite;
    75	        }
    76	        
    77	        @keyframes scroll-left {
    78	            0% { transform: translateX(100%); }
    79	            100% { transform: translateX(-100%); }
    80	        }
    81	        
    82	        /* ===== Header ===== */
    83	        .header {
    84	            background: var(--white);
    85	            border-bottom: 4px solid var(--brazil-green);
    86	            box-shadow: var(--shadow);
    87	            position: sticky;
    88	            top: 0;
    89	            z-index: 1000;
    90	        }
    91	        
    92	        .header-top {
    93	            max-width: 1400px;
    94	            margin: 0 auto;
    95	            padding: 20px 30px;
    96	            display: flex;
    97	            align-items: center;
    98	            justify-content: space-between;
    99	            gap: 30px;
   100	        }
   101	        
   102	        .logo {
   103	            display: flex;
   104	            flex-direction: column;
   105	            align-items: center;
   106	        }
   107	        
   108	        .logo-main {
   109	            font-size: 3rem;
   110	            font-weight: 700;
   111	            background: linear-gradient(135deg, var(--brazil-green) 0%, var(--brazil-yellow) 100%);
   112	            -webkit-background-clip: text;
   113	            -webkit-text-fill-color: transparent;
   114	            background-clip: text;
   115	            letter-spacing: 2px;
   116	            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
   117	        }
   118	        
   119	        .logo-subtitle {
   120	            font-size: 0.7rem;
   121	            color: var(--text-gray);
   122	            letter-spacing: 3px;
   123	            font-weight: 500;
   124	            margin-top: -5px;
   125	        }
   126	        
   127	        .search-box {
   128	            flex: 1;
   129	            max-width: 500px;
   130	            position: relative;
   131	        }
   132	        
   133	        .search-input {
   134	            width: 100%;
   135	            padding: 12px 45px 12px 20px;
   136	            border: 2px solid var(--border-light);
   137	            border-radius: 25px;
   138	            font-size: 0.95rem;
   139	            transition: all 0.3s ease;
   140	        }
   141	        
   142	        .search-input:focus {
   143	            outline: none;
   144	            border-color: var(--brazil-green);
   145	            box-shadow: 0 0 0 3px rgba(0, 156, 59, 0.1);
   146	        }
   147	        
   148	        .search-btn {
   149	            position: absolute;
   150	            right: 5px;
   151	            top: 50%;
   152	            transform: translateY(-50%);
   153	            background: var(--brazil-green);
   154	            color: var(--white);
   155	            border: none;
   156	            padding: 10px 18px;
   157	            border-radius: 20px;
   158	            cursor: pointer;
   159	            transition: all 0.3s ease;
   160	        }
   161	        
   162	        .search-btn:hover {
   163	            background: var(--brazil-blue);
   164	        }
   165	        
   166	        .header-icons {
   167	            display: flex;
   168	            gap: 15px;
   169	            font-size: 1.3rem;
   170	        }
   171	        
   172	        .header-icons a {
   173	            color: var(--text-gray);
   174	            transition: color 0.3s ease;
   175	        }
   176	        
   177	        .header-icons a:hover {
   178	            color: var(--brazil-green);
   179	        }
   180	        
   181	        /* ===== Navigation ===== */
   182	        .nav {
   183	            background: var(--brazil-green);
   184	            border-bottom: 3px solid var(--brazil-yellow);
   185	        }
   186	        
   187	        .nav-container {
   188	            max-width: 1400px;
   189	            margin: 0 auto;
   190	            display: flex;
   191	            justify-content: center;
   192	            align-items: center;
   193	        }
   194	        
   195	        .nav-menu {
   196	            display: flex;
   197	            flex-wrap: wrap;
   198	            justify-content: center;
   199	            gap: 5px;
   200	        }
   201	        
   202	        .nav-item {
   203	            position: relative;
   204	        }
   205	        
   206	        .nav-link {
   207	            display: block;
   208	            padding: 15px 22px;
   209	            color: var(--white);
   210	            font-weight: 500;
   211	            font-size: 0.95rem;
   212	            transition: all 0.3s ease;
   213	            position: relative;
   214	        }
   215	        
   216	        .nav-link::after {
   217	            content: '';
   218	            position: absolute;
   219	            bottom: 0;
   220	            left: 50%;
   221	            transform: translateX(-50%);
   222	            width: 0;
   223	            height: 3px;
   224	            background: var(--brazil-yellow);
   225	            transition: width 0.3s ease;
   226	        }
   227	        
   228	        .nav-link:hover {
   229	            background: rgba(255, 223, 0, 0.15);
   230	        }
   231	        
   232	        .nav-link:hover::after {
   233	            width: 80%;
   234	        }
   235	        
   236	        .mobile-toggle {
   237	            display: none;
   238	            background: var(--brazil-green);
   239	            color: var(--white);
   240	            border: none;
   241	            font-size: 1.5rem;
   242	            padding: 10px 15px;
   243	            cursor: pointer;
   244	        }
   245	        
   246	        /* ===== Main Container ===== */
   247	        .container {
   248	            max-width: 1400px;
   249	            margin: 0 auto;
   250	            padding: 40px 30px;
   251	            display: grid;
   252	            grid-template-columns: 1fr 350px;
   253	            gap: 40px;
   254	        }
   255	        
   256	        /* ===== Ad Banner (Top) ===== */
   257	        .ad-banner-top {
   258	            background: linear-gradient(135deg, var(--bg-light) 0%, #fff 100%);
   259	            border: 2px dashed var(--border-light);
   260	            padding: 20px;
   261	            text-align: center;
   262	            margin-bottom: 30px;
   263	            border-radius: 8px;
   264	            min-height: 90px;
   265	            display: flex;
   266	            align-items: center;
   267	            justify-content: center;
   268	            color: var(--text-gray);
   269	            font-size: 0.9rem;
   270	        }
   271	        
   272	        /* ===== Hero Section ===== */
   273	        .hero {
   274	            margin-bottom: 40px;
   275	        }
   276	        
   277	        .hero-card {
   278	            position: relative;
   279	            overflow: hidden;
   280	            border-radius: 12px;
   281	            box-shadow: var(--shadow);
   282	            height: 500px;
   283	            background: linear-gradient(135deg, var(--brazil-green) 0%, var(--brazil-blue) 100%);
   284	        }
   285	        
   286	        .hero-image {
   287	            width: 100%;
   288	            height: 100%;
   289	            object-fit: cover;
   290	            opacity: 0.85;
   291	            transition: transform 0.5s ease;
   292	        }
   293	        
   294	        .hero-card:hover .hero-image {
   295	            transform: scale(1.05);
   296	        }
   297	        
   298	        .hero-content {
   299	            position: absolute;
   300	            bottom: 0;
   301	            left: 0;
   302	            right: 0;
   303	            background: linear-gradient(to top, rgba(0,0,0,0.9) 0%, rgba(0,0,0,0.6) 70%, transparent 100%);
   304	            padding: 40px 35px;
   305	            color: var(--white);
   306	        }
   307	        
   308	        .hero-category {
   309	            display: inline-block;
   310	            background: var(--brazil-yellow);
   311	            color: var(--text-dark);
   312	            padding: 6px 18px;
   313	            border-radius: 20px;
   314	            font-size: 0.85rem;
   315	            font-weight: 600;
   316	            margin-bottom: 15px;
   317	        }
   318	        
   319	        .hero-title {
   320	            font-size: 2.2rem;
   321	            font-weight: 700;
   322	            line-height: 1.3;
   323	            margin-bottom: 12px;
   324	            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
   325	        }
   326	        
   327	        .hero-excerpt {
   328	            font-size: 1.05rem;
   329	            line-height: 1.6;
   330	            margin-bottom: 15px;
   331	            opacity: 0.95;
   332	        }
   333	        
   334	        .hero-meta {
   335	            display: flex;
   336	            align-items: center;
   337	            gap: 20px;
   338	            font-size: 0.9rem;
   339	            opacity: 0.9;
   340	        }
   341	        
   342	        /* ===== Section Title ===== */
   343	        .section-title {
   344	            font-size: 1.8rem;
   345	            font-weight: 700;
   346	            color: var(--text-dark);
   347	            margin-bottom: 25px;
   348	            padding-bottom: 12px;
   349	            border-bottom: 4px solid var(--brazil-green);
   350	            position: relative;
   351	        }
   352	        
   353	        .section-title::after {
   354	            content: '';
   355	            position: absolute;
   356	            bottom: -4px;
   357	            left: 0;
   358	            width: 100px;
   359	            height: 4px;
   360	            background: var(--brazil-yellow);
   361	        }
   362	        
   363	        /* ===== Article Grid ===== */
   364	        .articles-grid {
   365	            display: grid;
   366	            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
   367	            gap: 30px;
   368	            margin-bottom: 50px;
   369	        }
   370	        
   371	        .article-card {
   372	            background: var(--white);
   373	            border-radius: 10px;
   374	            overflow: hidden;
   375	            box-shadow: var(--shadow);
   376	            transition: all 0.3s ease;
   377	            display: flex;
   378	            flex-direction: column;
   379	        }
   380	        
   381	        .article-card:hover {
   382	            transform: translateY(-5px);
   383	            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
   384	        }
   385	        
   386	        .article-image {
   387	            width: 100%;
   388	            height: 220px;
   389	            object-fit: cover;
   390	            transition: transform 0.5s ease;
   391	        }
   392	        
   393	        .article-card:hover .article-image {
   394	            transform: scale(1.08);
   395	        }
   396	        
   397	        .article-image-wrapper {
   398	            overflow: hidden;
   399	            position: relative;
   400	        }
   401	        
   402	        .article-content {
   403	            padding: 22px;
   404	            flex: 1;
   405	            display: flex;
   406	            flex-direction: column;
   407	        }
   408	        
   409	        .article-category {
   410	            display: inline-block;
   411	            background: var(--brazil-green);
   412	            color: var(--white);
   413	            padding: 5px 14px;
   414	            border-radius: 15px;
   415	            font-size: 0.75rem;
   416	            font-weight: 600;
   417	            margin-bottom: 12px;
   418	            align-self: flex-start;
   419	        }
   420	        
   421	        .article-title {
   422	            font-size: 1.15rem;
   423	            font-weight: 600;
   424	            line-height: 1.5;
   425	            margin-bottom: 10px;
   426	            color: var(--text-dark);
   427	            flex: 1;
   428	        }
   429	        
   430	        .article-title:hover {
   431	            color: var(--brazil-green);
   432	        }
   433	        
   434	        .article-excerpt {
   435	            font-size: 0.9rem;
   436	            color: var(--text-gray);
   437	            line-height: 1.6;
   438	            margin-bottom: 15px;
   439	        }
   440	        
   441	        .article-meta {
   442	            display: flex;
   443	            align-items: center;
   444	            justify-content: space-between;
   445	            font-size: 0.8rem;
   446	            color: var(--text-gray);
   447	            padding-top: 12px;
   448	            border-top: 1px solid var(--border-light);
   449	        }
   450	        
   451	        .article-date {
   452	            display: flex;
   453	            align-items: center;
   454	            gap: 5px;
   455	        }
   456	        
   457	        .article-author {
   458	            display: flex;
   459	            align-items: center;
   460	            gap: 5px;
   461	        }
   462	        
   463	        /* ===== Sidebar ===== */
   464	        .sidebar {
   465	            position: sticky;
   466	            top: 120px;
   467	            height: fit-content;
   468	        }
   469	        
   470	        .sidebar-widget {
   471	            background: var(--white);
   472	            border-radius: 10px;
   473	            padding: 25px;
   474	            margin-bottom: 30px;
   475	            box-shadow: var(--shadow);
   476	        }
   477	        
   478	        .widget-title {
   479	            font-size: 1.3rem;
   480	            font-weight: 700;
   481	            color: var(--text-dark);
   482	            margin-bottom: 20px;
   483	            padding-bottom: 10px;
   484	            border-bottom: 3px solid var(--brazil-green);
   485	            position: relative;
   486	        }
   487	        
   488	        .widget-title::after {
   489	            content: '';
   490	            position: absolute;
   491	            bottom: -3px;
   492	            left: 0;
   493	            width: 60px;
   494	            height: 3px;
   495	            background: var(--brazil-yellow);
   496	        }
   497	        
   498	        /* Ad Banner (Sidebar) */
   499	        .ad-banner-sidebar {
   500	            background: linear-gradient(135deg, var(--bg-light) 0%, #fff 100%);
   501	            border: 2px dashed var(--border-light);
   502	            padding: 20px;
   503	            text-align: center;
   504	            border-radius: 8px;
   505	            min-height: 250px;
   506	            display: flex;
   507	            align-items: center;
   508	            justify-content: center;
   509	            color: var(--text-gray);
   510	            font-size: 0.85rem;
   511	            margin-bottom: 30px;
   512	        }
   513	        
   514	        .ad-banner-sidebar.large {
   515	            min-height: 600px;
   516	        }
   517	        
   518	        /* Popular Articles */
   519	        .popular-list {
   520	            display: flex;
   521	            flex-direction: column;
   522	            gap: 18px;
   523	        }
   524	        
   525	        .popular-item {
   526	            display: flex;
   527	            gap: 15px;
   528	            padding-bottom: 18px;
   529	            border-bottom: 1px solid var(--border-light);
   530	        }
   531	        
   532	        .popular-item:last-child {
   533	            border-bottom: none;
   534	            padding-bottom: 0;
   535	        }
   536	        
   537	        .popular-number {
   538	            font-size: 1.5rem;
   539	            font-weight: 700;
   540	            color: var(--brazil-green);
   541	            min-width: 30px;
   542	        }
   543	        
   544	        .popular-content h4 {
   545	            font-size: 0.95rem;
   546	            font-weight: 600;
   547	            line-height: 1.5;
   548	            margin-bottom: 5px;
   549	            color: var(--text-dark);
   550	        }
   551	        
   552	        .popular-content h4:hover {
   553	            color: var(--brazil-green);
   554	        }
   555	        
   556	        .popular-date {
   557	            font-size: 0.75rem;
   558	            color: var(--text-gray);
   559	        }
   560	        
   561	        /* Category List */
   562	        .category-list {
   563	            display: flex;
   564	            flex-direction: column;
   565	            gap: 10px;
   566	        }
   567	        
   568	        .category-item {
   569	            padding: 12px 15px;
   570	            background: var(--bg-light);
   571	            border-radius: 8px;
   572	            display: flex;
   573	            justify-content: space-between;
   574	            align-items: center;
   575	            transition: all 0.3s ease;
   576	            border-left: 4px solid var(--brazil-green);
   577	        }
   578	        
   579	        .category-item:hover {
   580	            background: var(--brazil-green);
   581	            color: var(--white);
   582	            transform: translateX(5px);
   583	        }
   584	        
   585	        .category-count {
   586	            background: var(--white);
   587	            padding: 3px 10px;
   588	            border-radius: 12px;
   589	            font-size: 0.8rem;
   590	            font-weight: 600;
   591	        }
   592	        
   593	        /* ===== Columnists Section ===== */
   594	        .columnists-section {
   595	            margin-top: 60px;
   596	            margin-bottom: 60px;
   597	        }
   598	        
   599	        .columnists-grid {
   600	            display: grid;
   601	            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
   602	            gap: 30px;
   603	        }
   604	        
   605	        .columnist-card {
   606	            background: var(--white);
   607	            border-radius: 10px;
   608	            padding: 30px;
   609	            text-align: center;
   610	            box-shadow: var(--shadow);
   611	            transition: all 0.3s ease;
   612	            border-top: 4px solid var(--brazil-green);
   613	        }
   614	        
   615	        .columnist-card:hover {
   616	            transform: translateY(-5px);
   617	            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
   618	            border-top-color: var(--brazil-yellow);
   619	        }
   620	        
   621	        .columnist-avatar {
   622	            width: 120px;
   623	            height: 120px;
   624	            border-radius: 50%;
   625	            background: linear-gradient(135deg, var(--brazil-green) 0%, var(--brazil-yellow) 100%);
   626	            margin: 0 auto 20px;
   627	            display: flex;
   628	            align-items: center;
   629	            justify-content: center;
   630	            font-size: 3rem;
   631	            color: var(--white);
   632	            border: 4px solid var(--white);
   633	            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
   634	        }
   635	        
   636	        .columnist-name {
   637	            font-size: 1.3rem;
   638	            font-weight: 700;
   639	            color: var(--text-dark);
   640	            margin-bottom: 8px;
   641	        }
   642	        
   643	        .columnist-column {
   644	            font-size: 0.9rem;
   645	            color: var(--brazil-green);
   646	            font-weight: 600;
   647	            margin-bottom: 15px;
   648	        }
   649	        
   650	        .columnist-bio {
   651	            font-size: 0.85rem;
   652	            color: var(--text-gray);
   653	            line-height: 1.6;
   654	            margin-bottom: 15px;
   655	        }
   656	        
   657	        .columnist-link {
   658	            display: inline-block;
   659	            color: var(--brazil-green);
   660	            font-weight: 600;
   661	            font-size: 0.9rem;
   662	            padding: 8px 20px;
   663	            border: 2px solid var(--brazil-green);
   664	            border-radius: 20px;
   665	            transition: all 0.3s ease;
   666	        }
   667	        
   668	        .columnist-link:hover {
   669	            background: var(--brazil-green);
   670	            color: var(--white);
   671	        }
   672	        
   673	        /* ===== Contact Form Section ===== */
   674	        .contact-section {
   675	            background: var(--bg-light);
   676	            padding: 60px 30px;
   677	            margin-top: 60px;
   678	        }
   679	        
   680	        .contact-container {
   681	            max-width: 800px;
   682	            margin: 0 auto;
   683	            background: var(--white);
   684	            padding: 50px;
   685	            border-radius: 12px;
   686	            box-shadow: var(--shadow);
   687	        }
   688	        
   689	        .contact-form {
   690	            display: flex;
   691	            flex-direction: column;
   692	            gap: 25px;
   693	        }
   694	        
   695	        .form-group {
   696	            display: flex;
   697	            flex-direction: column;
   698	            gap: 8px;
   699	        }
   700	        
   701	        .form-label {
   702	            font-weight: 600;
   703	            color: var(--text-dark);
   704	            font-size: 0.95rem;
   705	        }
   706	        
   707	        .form-label .required {
   708	            color: #e74c3c;
   709	            margin-left: 3px;
   710	        }
   711	        
   712	        .form-input,
   713	        .form-select,
   714	        .form-textarea {
   715	            padding: 12px 18px;
   716	            border: 2px solid var(--border-light);
   717	            border-radius: 8px;
   718	            font-size: 1rem;
   719	            font-family: inherit;
   720	            transition: all 0.3s ease;
   721	        }
   722	        
   723	        .form-input:focus,
   724	        .form-select:focus,
   725	        .form-textarea:focus {
   726	            outline: none;
   727	            border-color: var(--brazil-green);
   728	            box-shadow: 0 0 0 3px rgba(0, 156, 59, 0.1);
   729	        }
   730	        
   731	        .form-textarea {
   732	            min-height: 150px;
   733	            resize: vertical;
   734	        }
   735	        
   736	        .form-submit {
   737	            background: var(--brazil-green);
   738	            color: var(--white);
   739	            padding: 15px 40px;
   740	            border: none;
   741	            border-radius: 30px;
   742	            font-size: 1.1rem;
   743	            font-weight: 600;
   744	            cursor: pointer;
   745	            transition: all 0.3s ease;
   746	            align-self: flex-start;
   747	        }
   748	        
   749	        .form-submit:hover {
   750	            background: var(--brazil-blue);
   751	            transform: translateY(-2px);
   752	            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
   753	        }
   754	        
   755	        /* ===== Footer ===== */
   756	        .footer {
   757	            background: linear-gradient(180deg, #1a1a1a 0%, #000 100%);
   758	            color: #ccc;
   759	            padding: 60px 30px 30px;
   760	            border-top: 4px solid var(--brazil-green);
   761	        }
   762	        
   763	        .footer-stripe {
   764	            height: 4px;
   765	            background: linear-gradient(90deg, var(--brazil-green) 0%, var(--brazil-yellow) 50%, var(--brazil-blue) 100%);
   766	            margin-bottom: 40px;
   767	        }
   768	        
   769	        .footer-content {
   770	            max-width: 1400px;
   771	            margin: 0 auto;
   772	            display: grid;
   773	            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
   774	            gap: 40px;
   775	            margin-bottom: 40px;
   776	        }
   777	        
   778	        .footer-section h3 {
   779	            color: var(--white);
   780	            font-size: 1.2rem;
   781	            margin-bottom: 20px;
   782	            font-weight: 700;
   783	        }
   784	        
   785	        .footer-logo {
   786	            font-size: 2.5rem;
   787	            font-weight: 700;
   788	            background: linear-gradient(135deg, var(--brazil-green) 0%, var(--brazil-yellow) 100%);
   789	            -webkit-background-clip: text;
   790	            -webkit-text-fill-color: transparent;
   791	            background-clip: text;
   792	            margin-bottom: 15px;
   793	        }
   794	        
   795	        .footer-description {
   796	            line-height: 1.7;
   797	            margin-bottom: 20px;
   798	        }
   799	        
   800	        .footer-links {
   801	            display: flex;
   802	            flex-direction: column;
   803	            gap: 12px;
   804	        }
   805	        
   806	        .footer-links a {
   807	            color: #ccc;
   808	            transition: all 0.3s ease;
   809	            padding-left: 15px;
   810	            position: relative;
   811	        }
   812	        
   813	        .footer-links a::before {
   814	            content: '▸';
   815	            position: absolute;
   816	            left: 0;
   817	            color: var(--brazil-yellow);
   818	        }
   819	        
   820	        .footer-links a:hover {
   821	            color: var(--brazil-yellow);
   822	            padding-left: 20px;
   823	        }
   824	        
   825	        .social-links {
   826	            display: flex;
   827	            gap: 15px;
   828	            font-size: 1.5rem;
   829	        }
   830	        
   831	        .social-links a {
   832	            color: #ccc;
   833	            transition: all 0.3s ease;
   834	        }
   835	        
   836	        .social-links a:hover {
   837	            color: var(--brazil-green);
   838	            transform: translateY(-3px);
   839	        }
   840	        
   841	        .footer-bottom {
   842	            max-width: 1400px;
   843	            margin: 0 auto;
   844	            padding-top: 30px;
   845	            border-top: 1px solid #333;
   846	            text-align: center;
   847	            font-size: 0.9rem;
   848	            color: #888;
   849	        }
   850	        
   851	        /* ===== Responsive Design ===== */
   852	        @media (max-width: 1200px) {
   853	            .container {
   854	                grid-template-columns: 1fr;
   855	            }
   856	            
   857	            .sidebar {
   858	                position: static;
   859	            }
   860	            
   861	            .articles-grid {
   862	                grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
   863	            }
   864	        }
   865	        
   866	        @media (max-width: 768px) {
   867	            .header-top {
   868	                flex-direction: column;
   869	                gap: 20px;
   870	                padding: 20px;
   871	            }
   872	            
   873	            .logo-main {
   874	                font-size: 2.5rem;
   875	            }
   876	            
   877	            .search-box {
   878	                max-width: 100%;
   879	            }
   880	            
   881	            .mobile-toggle {
   882	                display: block;
   883	                position: absolute;
   884	                right: 20px;
   885	                top: 20px;
   886	            }
   887	            
   888	            .nav-menu {
   889	                display: none;
   890	                flex-direction: column;
   891	                width: 100%;
   892	            }
   893	            
   894	            .nav-menu.active {
   895	                display: flex;
   896	            }
   897	            
   898	            .nav-link {
   899	                text-align: center;
   900	                border-bottom: 1px solid rgba(255,255,255,0.1);
   901	            }
   902	            
   903	            .hero-card {
   904	                height: 400px;
   905	            }
   906	            
   907	            .hero-title {
   908	                font-size: 1.6rem;
   909	            }
   910	            
   911	            .articles-grid {
   912	                grid-template-columns: 1fr;
   913	            }
   914	            
   915	            .columnists-grid {
   916	                grid-template-columns: 1fr;
   917	            }
   918	            
   919	            .contact-container {
   920	                padding: 30px 20px;
   921	            }
   922	            
   923	            .footer-content {
   924	                grid-template-columns: 1fr;
   925	            }
   926	        }
   927	        
   928	        @media (max-width: 480px) {
   929	            .container {
   930	                padding: 20px 15px;
   931	            }
   932	            
   933	            .logo-main {
   934	                font-size: 2rem;
   935	            }
   936	            
   937	            .hero-card {
   938	                height: 350px;
   939	            }
   940	            
   941	            .hero-title {
   942	                font-size: 1.4rem;
   943	            }
   944	            
   945	            .section-title {
   946	                font-size: 1.5rem;
   947	            }
   948	        }
   949	        
   950	        /* ===== Utility Classes ===== */
   951	        .text-center {
   952	            text-align: center;
   953	        }
   954	        
   955	        .mt-1 { margin-top: 10px; }
   956	        .mt-2 { margin-top: 20px; }
   957	        .mt-3 { margin-top: 30px; }
   958	        .mb-1 { margin-bottom: 10px; }
   959	        .mb-2 { margin-bottom: 20px; }
   960	        .mb-3 { margin-bottom: 30px; }
   961	    </style>
   962	</head>
   963	<body>
   964	    <!-- Top News Bar -->
   965	    <div class="top-bar">
   966	        <div class="top-bar-content">
   967	            ★ 最新ニュース：サンパウロ日系協会が創立100周年記念イベント開催 | リベルダージに新オープン！本格和食レストラン3店舗 | ブラジルワーホリビザ申請受付中！詳細はこちら ★
   968	        </div>
   969	    </div>
   970	
   971	    <!-- Header -->
   972	    <header class="header">
   973	        <div class="header-top">
   974	            <a href="index.html" class="logo">
   975	                <div class="logo-main">SAMPA</div>
   976	                <div class="logo-subtitle">SÃO PAULO × JAPAN MAGAZINE</div>
   977	            </a>
   978	            
   979	            <div class="search-box">
   980	                <input type="text" class="search-input" placeholder="記事を検索..." id="searchInput">
   981	                <button class="search-btn" onclick="performSearch()">
   982	                    <i class="fas fa-search"></i>
   983	                </button>
   984	            </div>
   985	            
   986	            <div class="header-icons">
   987	                <a href="#" title="Facebook"><i class="fab fa-facebook"></i></a>
   988	                <a href="#" title="Instagram"><i class="fab fa-instagram"></i></a>
   989	                <a href="#" title="LINE"><i class="fab fa-line"></i></a>
   990	                <a href="#" title="YouTube"><i class="fab fa-youtube"></i></a>
   991	            </div>
   992	        </div>
   993	        
   994	        <!-- Navigation -->
   995	        <nav class="nav">
   996	            <button class="mobile-toggle" onclick="toggleMenu()">
   997	                <i class="fas fa-bars"></i>
   998	            </button>
   999	            <div class="nav-container">
  1000	                <ul class="nav-menu" id="navMenu">
  1001	                    <li class="nav-item"><a href="#" class="nav-link">ホーム</a></li>
  1002	                    <li class="nav-item"><a href="#gourmet" class="nav-link">グルメ</a></li>
  1003	                    <li class="nav-item"><a href="#lifestyle" class="nav-link">ライフスタイル</a></li>
  1004	                    <li class="nav-item"><a href="#business" class="nav-link">ビジネス</a></li>
  1005	                    <li class="nav-item"><a href="#culture" class="nav-link">カルチャー</a></li>
  1006	                    <li class="nav-item"><a href="#community" class="nav-link">コミュニティ</a></li>
  1007	                    <li class="nav-item"><a href="#working-holiday" class="nav-link">ワーホリ・留学</a></li>
  1008	                    <li class="nav-item"><a href="#health-beauty" class="nav-link">健康・美容</a></li>
  1009	                    <li class="nav-item"><a href="#travel" class="nav-link">トラベル</a></li>
  1010	                    <li class="nav-item"><a href="#contact" class="nav-link">お問い合わせ</a></li>
  1011	                </ul>
  1012	            </div>
  1013	        </nav>
  1014	    </header>
  1015	
  1016	    <!-- Main Container -->
  1017	    <div class="container">
  1018	        <!-- Main Content -->
  1019	        <main class="main-content">
  1020	            <!-- Ad Banner (Top) -->
  1021	            <div class="ad-banner-top" data-ad="728x90">
  1022	                <p><i class="fas fa-ad"></i> 広告スペース (728×90)</p>
  1023	            </div>
  1024	
  1025	            <!-- Hero Section -->
  1026	            <section class="hero">
  1027	                <a href="#" class="hero-card">
  1028	                    <img src="https://images.unsplash.com/photo-1555396273-367ea4eb4db5?w=1200&h=600&fit=crop" alt="サンパウロ美食探訪" class="hero-image">
  1029	                    <div class="hero-content">
  1030	                        <span class="hero-category">グルメ</span>
  1031	                        <h2 class="hero-title">リベルダージの新星！本格サンパウロラーメン店3選</h2>
  1032	                        <p class="hero-excerpt">サンパウロの日本人街リベルダージに続々とオープンしている本格ラーメン店。今回は、地元日本人が絶賛する3店舗を徹底取材しました。</p>
  1033	                        <div class="hero-meta">
  1034	                            <span><i class="far fa-calendar"></i> 2025年2月26日</span>
  1035	                            <span><i class="far fa-user"></i> 編集部</span>
  1036	                        </div>
  1037	                    </div>
  1038	                </a>
  1039	            </section>
  1040	
  1041	            <!-- Latest Articles -->
  1042	            <section class="latest-articles">
  1043	                <h2 class="section-title">最新記事</h2>
  1044	                <div class="articles-grid" id="articlesGrid">
  1045	                    <!-- Article 1 -->
  1046	                    <article class="article-card">
  1047	                        <div class="article-image-wrapper">
  1048	                            <img src="https://images.unsplash.com/photo-1564489563601-c53cfc451e93?w=400&h=250&fit=crop" alt="パウリスタ大通り" class="article-image">
  1049	                        </div>
  1050	                        <div class="article-content">
  1051	                            <span class="article-category">グルメ</span>
  1052	                            <h3 class="article-title">パウリスタ大通りで見つけた絶品日本食レストラン</h3>
  1053	                            <p class="article-excerpt">サンパウロのメインストリート、パウリスタ大通り周辺で楽しめる本格日本食レストランをご紹介。寿司、ラーメン、居酒屋まで完全網羅。</p>
  1054	                            <div class="article-meta">
  1055	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.26</span>
  1056	                                <span class="article-author"><i class="far fa-user"></i> 田中美咲</span>
  1057	                            </div>
  1058	                        </div>
  1059	                    </article>
  1060	
  1061	                    <!-- Article 2 -->
  1062	                    <article class="article-card">
  1063	                        <div class="article-image-wrapper">
  1064	                            <img src="https://images.unsplash.com/photo-1586297098710-0382a496c814?w=400&h=250&fit=crop" alt="ブラジルスーパー" class="article-image">
  1065	                        </div>
  1066	                        <div class="article-content">
  1067	                            <span class="article-category">グルメ</span>
  1068	                            <h3 class="article-title">ブラジルスーパーで買えるお薦め食材7選</h3>
  1069	                            <p class="article-excerpt">日本食材が手に入りにくいブラジルで、現地スーパーで買える日本料理に使える食材を厳選してご紹介します。</p>
  1070	                            <div class="article-meta">
  1071	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.25</span>
  1072	                                <span class="article-author"><i class="far fa-user"></i> 佐藤健太</span>
  1073	                            </div>
  1074	                        </div>
  1075	                    </article>
  1076	
  1077	                    <!-- Article 3 -->
  1078	                    <article class="article-card">
  1079	                        <div class="article-image-wrapper">
  1080	                            <img src="https://images.unsplash.com/photo-1560448204-e02f11c3d0e2?w=400&h=250&fit=crop" alt="サンパウロ住まい" class="article-image">
  1081	                        </div>
  1082	                        <div class="article-content">
  1083	                            <span class="article-category">ライフスタイル</span>
  1084	                            <h3 class="article-title">サンパウロ駐在員が教える：快適な住まい探しの極意</h3>
  1085	                            <p class="article-excerpt">サンパウロで安全で快適な住まいを見つけるコツとは？駐在経験者が語る、エリア選びから契約まで完全ガイド。</p>
  1086	                            <div class="article-meta">
  1087	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.25</span>
  1088	                                <span class="article-author"><i class="far fa-user"></i> 山田太郎</span>
  1089	                            </div>
  1090	                        </div>
  1091	                    </article>
  1092	
  1093	                    <!-- Article 4 -->
  1094	                    <article class="article-card">
  1095	                        <div class="article-image-wrapper">
  1096	                            <img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?w=400&h=250&fit=crop" alt="日本語学校" class="article-image">
  1097	                        </div>
  1098	                        <div class="article-content">
  1099	                            <span class="article-category">ライフスタイル</span>
  1100	                            <h3 class="article-title">サンパウロで日本語学校に子供を通わせる方法</h3>
  1101	                            <p class="article-excerpt">サンパウロ市内とその周辺にある日本語学校の特徴や授業料、カリキュラムを徹底比較。お子さんの教育に最適な選択を。</p>
  1102	                            <div class="article-meta">
  1103	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.24</span>
  1104	                                <span class="article-author"><i class="far fa-user"></i> 鈴木花子</span>
  1105	                            </div>
  1106	                        </div>
  1107	                    </article>
  1108	
  1109	                    <!-- Article 5 -->
  1110	                    <article class="article-card">
  1111	                        <div class="article-image-wrapper">
  1112	                            <img src="https://images.unsplash.com/photo-1568605117036-5fe5e7bab0b7?w=400&h=250&fit=crop" alt="サンパウロ治安" class="article-image">
  1113	                        </div>
  1114	                        <div class="article-content">
  1115	                            <span class="article-category">ライフスタイル</span>
  1116	                            <h3 class="article-title">2025年版：サンパウロの治安事情と安全対策</h3>
  1117	                            <p class="article-excerpt">サンパウロで安全に暮らすために知っておくべき最新の治安情報と実践的な防犯対策をまとめました。</p>
  1118	                            <div class="article-meta">
  1119	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.24</span>
  1120	                                <span class="article-author"><i class="far fa-user"></i> 中村誠</span>
  1121	                            </div>
  1122	                        </div>
  1123	                    </article>
  1124	
  1125	                    <!-- Article 6 -->
  1126	                    <article class="article-card">
  1127	                        <div class="article-image-wrapper">
  1128	                            <img src="https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=400&h=250&fit=crop" alt="ブラジル起業" class="article-image">
  1129	                        </div>
  1130	                        <div class="article-content">
  1131	                            <span class="article-category">ビジネス</span>
  1132	                            <h3 class="article-title">ブラジルで会社設立：日本人起業家が知るべき10のこと</h3>
  1133	                            <p class="article-excerpt">ブラジルでビジネスを始めるために必要な手続き、税制、法律について、実際の起業家がアドバイスします。</p>
  1134	                            <div class="article-meta">
  1135	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.23</span>
  1136	                                <span class="article-author"><i class="far fa-user"></i> 高橋大輔</span>
  1137	                            </div>
  1138	                        </div>
  1139	                    </article>
  1140	
  1141	                    <!-- Article 7 -->
  1142	                    <article class="article-card">
  1143	                        <div class="article-image-wrapper">
  1144	                            <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=400&h=250&fit=crop" alt="ITエンジニア" class="article-image">
  1145	                        </div>
  1146	                        <div class="article-content">
  1147	                            <span class="article-category">ビジネス</span>
  1148	                            <h3 class="article-title">サンパウロのIT業界：日本人エンジニアの実態</h3>
  1149	                            <p class="article-excerpt">急成長するブラジルのIT業界で働く日本人エンジニアたち。給与、労働環境、キャリアパスなど、リアルな声をお届け。</p>
  1150	                            <div class="article-meta">
  1151	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.23</span>
  1152	                                <span class="article-author"><i class="far fa-user"></i> 吉田拓也</span>
  1153	                            </div>
  1154	                        </div>
  1155	                    </article>
  1156	
  1157	                    <!-- Article 8 -->
  1158	                    <article class="article-card">
  1159	                        <div class="article-image-wrapper">
  1160	                            <img src="https://images.unsplash.com/photo-1533158326339-7f3cf2404354?w=400&h=250&fit=crop" alt="日本移民" class="article-image">
  1161	                        </div>
  1162	                        <div class="article-content">
  1163	                            <span class="article-category">カルチャー</span>
  1164	                            <h3 class="article-title">ブラジル日本移民115周年：歴史を振り返る</h3>
  1165	                            <p class="article-excerpt">1910年から始まった日本人のブラジル移民。115年の歴史を写真と証言で振り返る特集記事。</p>
  1166	                            <div class="article-meta">
  1167	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.22</span>
  1168	                                <span class="article-author"><i class="far fa-user"></i> 小林史郎</span>
  1169	                            </div>
  1170	                        </div>
  1171	                    </article>
  1172	
  1173	                    <!-- Article 9 -->
  1174	                    <article class="article-card">
  1175	                        <div class="article-image-wrapper">
  1176	                            <img src="https://images.unsplash.com/photo-1613426728039-f0a3a852d87e?w=400&h=250&fit=crop" alt="ジャパンフェス" class="article-image">
  1177	                        </div>
  1178	                        <div class="article-content">
  1179	                            <span class="article-category">カルチャー</span>
  1180	                            <h3 class="article-title">サンパウロのジャパンカルチャーフェスレポート</h3>
  1181	                            <p class="article-excerpt">年々盛り上がりを見せるサンパウロのジャパンフェス。アニメ、マンガ、コスプレ、グルメまで盛りだくさんのイベントをレポート。</p>
  1182	                            <div class="article-meta">
  1183	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.22</span>
  1184	                                <span class="article-author"><i class="far fa-user"></i> 松本あゆみ</span>
  1185	                            </div>
  1186	                        </div>
  1187	                    </article>
  1188	
  1189	                    <!-- Article 10 -->
  1190	                    <article class="article-card">
  1191	                        <div class="article-image-wrapper">
  1192	                            <img src="https://images.unsplash.com/photo-1541872705-1f73c6400ec9?w=400&h=250&fit=crop" alt="日本領事館" class="article-image">
  1193	                        </div>
  1194	                        <div class="article-content">
  1195	                            <span class="article-category">コミュニティ</span>
  1196	                            <h3 class="article-title">在サンパウロ日本国総領事館からのお知らせ</h3>
  1197	                            <p class="article-excerpt">パスポート更新、在留届、領事サービスなど、サンパウロ在住日本人が知っておくべき総領事館情報まとめ。</p>
  1198	                            <div class="article-meta">
  1199	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.21</span>
  1200	                                <span class="article-author"><i class="far fa-user"></i> 編集部</span>
  1201	                            </div>
  1202	                        </div>
  1203	                    </article>
  1204	
  1205	                    <!-- Article 11 -->
  1206	                    <article class="article-card">
  1207	                        <div class="article-image-wrapper">
  1208	                            <img src="https://images.unsplash.com/photo-1511795409834-ef04bbd61622?w=400&h=250&fit=crop" alt="日系人会" class="article-image">
  1209	                        </div>
  1210	                        <div class="article-content">
  1211	                            <span class="article-category">コミュニティ</span>
  1212	                            <h3 class="article-title">日系人会イベントカレンダー2025</h3>
  1213	                            <p class="article-excerpt">サンパウロ日系協会、文化センター、日本人会が主催する2025年の年間イベント情報を一挙公開！</p>
  1214	                            <div class="article-meta">
  1215	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.21</span>
  1216	                                <span class="article-author"><i class="far fa-user"></i> 編集部</span>
  1217	                            </div>
  1218	                        </div>
  1219	                    </article>
  1220	
  1221	                    <!-- Article 12 -->
  1222	                    <article class="article-card">
  1223	                        <div class="article-image-wrapper">
  1224	                            <img src="https://images.unsplash.com/photo-1488646953014-85cb44e25828?w=400&h=250&fit=crop" alt="ワーホリ体験" class="article-image">
  1225	                        </div>
  1226	                        <div class="article-content">
  1227	                            <span class="article-category">ワーホリ・留学</span>
  1228	                            <h3 class="article-title">ブラジルワーホリ体験記：サンパウロで1年間暮らした感想</h3>
  1229	                            <p class="article-excerpt">ワーキングホリデーでサンパウロに1年間滞在した筆者が語る、リアルなブラジル生活。仕事、住まい、友達づくりまで。</p>
  1230	                            <div class="article-meta">
  1231	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.20</span>
  1232	                                <span class="article-author"><i class="far fa-user"></i> 伊藤美咲</span>
  1233	                            </div>
  1234	                        </div>
  1235	                    </article>
  1236	
  1237	                    <!-- Article 13 -->
  1238	                    <article class="article-card">
  1239	                        <div class="article-image-wrapper">
  1240	                            <img src="https://images.unsplash.com/photo-1546410531-bb4caa6b424d?w=400&h=250&fit=crop" alt="ポルトガル語学校" class="article-image">
  1241	                        </div>
  1242	                        <div class="article-content">
  1243	                            <span class="article-category">ワーホリ・留学</span>
  1244	                            <h3 class="article-title">ポルトガル語学校比較：サンパウロ中心部おすすめ5校</h3>
  1245	                            <p class="article-excerpt">サンパウロでポルトガル語を学ぶなら？授業料、カリキュラム、日本人サポートなど、主要語学学校を徹底比較。</p>
  1246	                            <div class="article-meta">
  1247	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.20</span>
  1248	                                <span class="article-author"><i class="far fa-user"></i> 渡辺翔太</span>
  1249	                            </div>
  1250	                        </div>
  1251	                    </article>
  1252	
  1253	                    <!-- Article 14 -->
  1254	                    <article class="article-card">
  1255	                        <div class="article-image-wrapper">
  1256	                            <img src="https://images.unsplash.com/photo-1519494026892-80bbd2d6fd0d?w=400&h=250&fit=crop" alt="日本語対応クリニック" class="article-image">
  1257	                        </div>
  1258	                        <div class="article-content">
  1259	                            <span class="article-category">健康・美容</span>
  1260	                            <h3 class="article-title">サンパウロで日本語対応クリニック完全ガイド</h3>
  1261	                            <p class="article-excerpt">もしもの時に安心！サンパウロで日本語が通じる病院・クリニック情報と、医療保険の使い方を解説。</p>
  1262	                            <div class="article-meta">
  1263	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.19</span>
  1264	                                <span class="article-author"><i class="far fa-user"></i> 村上恵子</span>
  1265	                            </div>
  1266	                        </div>
  1267	                    </article>
  1268	
  1269	                    <!-- Article 15 -->
  1270	                    <article class="article-card">
  1271	                        <div class="article-image-wrapper">
  1272	                            <img src="https://images.unsplash.com/photo-1584308666744-24d5c474f2ae?w=400&h=250&fit=crop" alt="ブラジル薬" class="article-image">
  1273	                        </div>
  1274	                        <div class="article-content">
  1275	                            <span class="article-category">健康・美容</span>
  1276	                            <h3 class="article-title">ブラジルの市販薬と日本薬の違いを理解しよう</h3>
  1277	                            <p class="article-excerpt">薬局で買える市販薬、成分や効能の違いを知って賢く活用。日本から持ち込むべき薬もご紹介します。</p>
  1278	                            <div class="article-meta">
  1279	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.19</span>
  1280	                                <span class="article-author"><i class="far fa-user"></i> 加藤健一</span>
  1281	                            </div>
  1282	                        </div>
  1283	                    </article>
  1284	
  1285	                    <!-- Article 16 -->
  1286	                    <article class="article-card">
  1287	                        <div class="article-image-wrapper">
  1288	                            <img src="https://images.unsplash.com/photo-1559827260-dc66d52bef19?w=400&h=250&fit=crop" alt="サンパウロビーチ" class="article-image">
  1289	                        </div>
  1290	                        <div class="article-content">
  1291	                            <span class="article-category">トラベル</span>
  1292	                            <h3 class="article-title">サンパウロから日帰りで行けるビーチ5選</h3>
  1293	                            <p class="article-excerpt">週末のリフレッシュに最適！サンパウロから2時間以内でアクセスできる美しいビーチをご紹介。</p>
  1294	                            <div class="article-meta">
  1295	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.18</span>
  1296	                                <span class="article-author"><i class="far fa-user"></i> 森本愛美</span>
  1297	                            </div>
  1298	                        </div>
  1299	                    </article>
  1300	
  1301	                    <!-- Article 17 -->
  1302	                    <article class="article-card">
  1303	                        <div class="article-image-wrapper">
  1304	                            <img src="https://images.unsplash.com/photo-1564221710304-0b37c8b9d729?w=400&h=250&fit=crop" alt="イグアスの滝" class="article-image">
  1305	                        </div>
  1306	                        <div class="article-content">
  1307	                            <span class="article-category">トラベル</span>
  1308	                            <h3 class="article-title">イグアス滝への完全アクセスガイド</h3>
  1309	                            <p class="article-excerpt">世界三大瀑布の一つ、イグアスの滝。サンパウロからの行き方、ベストシーズン、見どころを徹底解説。</p>
  1310	                            <div class="article-meta">
  1311	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.18</span>
  1312	                                <span class="article-author"><i class="far fa-user"></i> 石井俊介</span>
  1313	                            </div>
  1314	                        </div>
  1315	                    </article>
  1316	
  1317	                    <!-- Article 18 -->
  1318	                    <article class="article-card">
  1319	                        <div class="article-image-wrapper">
  1320	                            <img src="https://images.unsplash.com/photo-1551218808-94e220e084d2?w=400&h=250&fit=crop" alt="フェイジョアーダ" class="article-image">
  1321	                        </div>
  1322	                        <div class="article-content">
  1323	                            <span class="article-category">グルメ</span>
  1324	                            <h3 class="article-title">本場のフェイジョアーダを食べるならこの店！</h3>
  1325	                            <p class="article-excerpt">ブラジルの国民食フェイジョアーダ。サンパウロで地元民が通う本格派レストランを厳選紹介。</p>
  1326	                            <div class="article-meta">
  1327	                                <span class="article-date"><i class="far fa-calendar"></i> 2025.02.17</span>
  1328	                                <span class="article-author"><i class="far fa-user"></i> 大野健太</span>
  1329	                            </div>
  1330	                        </div>
  1331	                    </article>
  1332	                </div>
  1333	            </section>
  1334	
  1335	            <!-- Ad Banner (Mid) -->
  1336	            <div class="ad-banner-top" data-ad="full-width" style="margin-top: 40px; margin-bottom: 40px;">
  1337	                <p><i class="fas fa-ad"></i> 広告スペース (全幅バナー)</p>
  1338	            </div>
  1339	
  1340	            <!-- Columnists Section -->
  1341	            <section class="columnists-section" id="columnists">
  1342	                <h2 class="section-title">注目のコラムニスト</h2>
  1343	                <div class="columnists-grid">
  1344	                    <!-- Columnist 1 -->
  1345	                    <div class="columnist-card">
  1346	                        <div class="columnist-avatar">
  1347	                            <i class="fas fa-user"></i>
  1348	                        </div>
  1349	                        <h3 class="columnist-name">田中美咲</h3>
  1350	                        <p class="columnist-column">サンパウロ美食探訪</p>
  1351	                        <p class="columnist-bio">サンパウロ在住15年。レストランジャーナリストとして、サンパウロの日本食シーンを取材中。</p>
  1352	                        <a href="#" class="columnist-link">記事一覧を見る</a>
  1353	                    </div>
  1354	
  1355	                    <!-- Columnist 2 -->
  1356	                    <div class="columnist-card">
  1357	                        <div class="columnist-avatar">
  1358	                            <i class="fas fa-user"></i>
  1359	                        </div>
  1360	                        <h3 class="columnist-name">山田太郎</h3>
  1361	                        <p class="columnist-column">ブラジル移住の記録</p>
  1362	                        <p class="columnist-bio">2020年にサンパウロに移住。駐在員として働きながら、ブラジル生活のリアルを発信。</p>
  1363	                        <a href="#" class="columnist-link">記事一覧を見る</a>
  1364	                    </div>
  1365	
  1366	                    <!-- Columnist 3 -->
  1367	                    <div class="columnist-card">
  1368	                        <div class="columnist-avatar">
  1369	                            <i class="fas fa-user"></i>
  1370	                        </div>
  1371	                        <h3 class="columnist-name">小林史郎</h3>
  1372	                        <p class="columnist-column">日系コミュニティNOW</p>
  1373	                        <p class="columnist-bio">日系三世として、ブラジルの日系コミュニティの今を伝える活動を続けています。</p>
  1374	                        <a href="#" class="columnist-link">記事一覧を見る</a>
  1375	                    </div>
  1376	
  1377	                    <!-- Columnist 4 -->
  1378	                    <div class="columnist-card">
  1379	                        <div class="columnist-avatar">
  1380	                            <i class="fas fa-user"></i>
  1381	                        </div>
  1382	                        <h3 class="columnist-name">高橋大輔</h3>
  1383	                        <p class="columnist-column">ブラジルビジネス最前線</p>
  1384	                        <p class="columnist-bio">サンパウロで起業し成功を収めた経営者。ブラジルビジネスの最新情報をお届けします。</p>
  1385	                        <a href="#" class="columnist-link">記事一覧を見る</a>
  1386	                    </div>
  1387	
  1388	                    <!-- Columnist 5 -->
  1389	                    <div class="columnist-card">
  1390	                        <div class="columnist-avatar">
  1391	                            <i class="fas fa-user"></i>
  1392	                        </div>
  1393	                        <h3 class="columnist-name">村上恵子</h3>
  1394	                        <p class="columnist-column">サンパウロ健康だより</p>
  1395	                        <p class="columnist-bio">看護師資格を持ち、ブラジルの医療事情に精通。在住者の健康をサポート。</p>
  1396	                        <a href="#" class="columnist-link">記事一覧を見る</a>
  1397	                    </div>
  1398	
  1399	                    <!-- Columnist 6 -->
  1400	                    <div class="columnist-card">
  1401	                        <div class="columnist-avatar">
  1402	                            <i class="fas fa-user"></i>
  1403	                        </div>
  1404	                        <h3 class="columnist-name">渡辺翔太</h3>
  1405	                        <p class="columnist-column">ポルトガル語マスター術</p>
  1406	                        <p class="columnist-bio">ポルトガル語講師として活躍。効率的な学習法とブラジルポルトガル語のコツを伝授。</p>
  1407	                        <a href="#" class="columnist-link">記事一覧を見る</a>
  1408	                    </div>
  1409	                </div>
  1410	            </section>
  1411	        </main>
  1412	
  1413	        <!-- Sidebar -->
  1414	        <aside class="sidebar">
  1415	            <!-- Ad Banner (Sidebar - Medium) -->
  1416	            <div class="ad-banner-sidebar" data-ad="300x250">
  1417	                <p><i class="fas fa-ad"></i> 広告スペース<br>(300×250)</p>
  1418	            </div>
  1419	
  1420	            <!-- Popular Articles -->
  1421	            <div class="sidebar-widget">
  1422	                <h3 class="widget-title">人気記事TOP5</h3>
  1423	                <div class="popular-list">
  1424	                    <a href="#" class="popular-item">
  1425	                        <div class="popular-number">1</div>
  1426	                        <div class="popular-content">
  1427	                            <h4>リベルダージの新星！本格サンパウロラーメン店3選</h4>
  1428	                            <span class="popular-date">2025.02.26</span>
  1429	                        </div>
  1430	                    </a>
  1431	                    <a href="#" class="popular-item">
  1432	                        <div class="popular-number">2</div>
  1433	                        <div class="popular-content">
  1434	                            <h4>サンパウロ駐在員が教える：快適な住まい探しの極意</h4>
  1435	                            <span class="popular-date">2025.02.25</span>
  1436	                        </div>
  1437	                    </a>
  1438	                    <a href="#" class="popular-item">
  1439	                        <div class="popular-number">3</div>
  1440	                        <div class="popular-content">
  1441	                            <h4>ブラジルで会社設立：日本人起業家が知るべき10のこと</h4>
  1442	                            <span class="popular-date">2025.02.23</span>
  1443	                        </div>
  1444	                    </a>
  1445	                    <a href="#" class="popular-item">
  1446	                        <div class="popular-number">4</div>
  1447	                        <div class="popular-content">
  1448	                            <h4>サンパウロで日本語対応クリニック完全ガイド</h4>
  1449	                            <span class="popular-date">2025.02.19</span>
  1450	                        </div>
  1451	                    </a>
  1452	                    <a href="#" class="popular-item">
  1453	                        <div class="popular-number">5</div>
  1454	                        <div class="popular-content">
  1455	                            <h4>イグアス滝への完全アクセスガイド</h4>
  1456	                            <span class="popular-date">2025.02.18</span>
  1457	                        </div>
  1458	                    </a>
  1459	                </div>
  1460	            </div>
  1461	
  1462	            <!-- Categories -->
  1463	            <div class="sidebar-widget">
  1464	                <h3 class="widget-title">カテゴリ</h3>
  1465	                <div class="category-list">
  1466	                    <a href="#gourmet" class="category-item">
  1467	                        <span><i class="fas fa-utensils"></i> グルメ</span>
  1468	                        <span class="category-count">24</span>
  1469	                    </a>
  1470	                    <a href="#lifestyle" class="category-item">
  1471	                        <span><i class="fas fa-home"></i> ライフスタイル</span>
  1472	                        <span class="category-count">32</span>
  1473	                    </a>
  1474	                    <a href="#business" class="category-item">
  1475	                        <span><i class="fas fa-briefcase"></i> ビジネス</span>
  1476	                        <span class="category-count">18</span>
  1477	                    </a>
  1478	                    <a href="#culture" class="category-item">
  1479	                        <span><i class="fas fa-palette"></i> カルチャー</span>
  1480	                        <span class="category-count">21</span>
  1481	                    </a>
  1482	                    <a href="#community" class="category-item">
  1483	                        <span><i class="fas fa-users"></i> コミュニティ</span>
  1484	                        <span class="category-count">15</span>
  1485	                    </a>
  1486	                    <a href="#working-holiday" class="category-item">
  1487	                        <span><i class="fas fa-plane"></i> ワーホリ・留学</span>
  1488	                        <span class="category-count">27</span>
  1489	                    </a>
  1490	                    <a href="#health-beauty" class="category-item">
  1491	                        <span><i class="fas fa-heartbeat"></i> 健康・美容</span>
  1492	                        <span class="category-count">19</span>
  1493	                    </a>
  1494	                    <a href="#travel" class="category-item">
  1495	                        <span><i class="fas fa-map-marked-alt"></i> トラベル</span>
  1496	                        <span class="category-count">22</span>
  1497	                    </a>
  1498	                </div>
  1499	            </div>
  1500	
  1501	            <!-- Ad Banner (Sidebar - Large) -->
  1502	            <div class="ad-banner-sidebar large" data-ad="300x600">
  1503	                <p><i class="fas fa-ad"></i> 広告スペース<br>(300×600)</p>
  1504	            </div>
  1505	        </aside>
  1506	    </div>
  1507	
  1508	    <!-- Contact Form Section -->
  1509	    <section class="contact-section" id="contact">
  1510	        <div class="contact-container">
  1511	            <h2 class="section-title text-center">お問い合わせ</h2>
  1512	            <p class="text-center mb-3" style="color: var(--text-gray);">
  1513	                広告掲載、コラム投稿、取材依頼など、お気軽にお問い合わせください。
  1514	            </p>
  1515	            <form class="contact-form" id="contactForm">
  1516	                <div class="form-group">
  1517	                    <label class="form-label">お名前 <span class="required">*</span></label>
  1518	                    <input type="text" class="form-input" required placeholder="山田太郎">
  1519	                </div>
  1520	                
  1521	                <div class="form-group">
  1522	                    <label class="form-label">メールアドレス <span class="required">*</span></label>
  1523	                    <input type="email" class="form-input" required placeholder="example@email.com">
  1524	                </div>
  1525	                
  1526	                <div class="form-group">
  1527	                    <label class="form-label">件名 <span class="required">*</span></label>
  1528	                    <select class="form-select" required>
  1529	                        <option value="">選択してください</option>
  1530	                        <option value="ad">広告掲載について</option>
  1531	                        <option value="column">コラム投稿について</option>
  1532	                        <option value="interview">取材依頼</option>
  1533	                        <option value="other">その他</option>
  1534	                    </select>
  1535	                </div>
  1536	                
  1537	                <div class="form-group">
  1538	                    <label class="form-label">メッセージ <span class="required">*</span></label>
  1539	                    <textarea class="form-textarea" required placeholder="お問い合わせ内容をご記入ください"></textarea>
  1540	                </div>
  1541	                
  1542	                <button type="submit" class="form-submit">送信する</button>
  1543	            </form>
  1544	        </div>
  1545	    </section>
  1546	
  1547	    <!-- Footer -->
  1548	    <footer class="footer">
  1549	        <div class="footer-stripe"></div>
  1550	        <div class="footer-content">
  1551	            <!-- About -->
  1552	            <div class="footer-section">
  1553	                <div class="footer-logo">SAMPA</div>
  1554	                <p class="footer-description">
  1555	                    サンパウロ在住日本人・日系人のための生活情報ウェブマガジン。グルメ、ライフスタイル、ビジネス、カルチャー情報を毎日更新中。
  1556	                </p>
  1557	                <div class="social-links">
  1558	                    <a href="#"><i class="fab fa-facebook"></i></a>
  1559	                    <a href="#"><i class="fab fa-instagram"></i></a>
  1560	                    <a href="#"><i class="fab fa-line"></i></a>
  1561	                    <a href="#"><i class="fab fa-youtube"></i></a>
  1562	                    <a href="#"><i class="fab fa-twitter"></i></a>
  1563	                </div>
  1564	            </div>
  1565	
  1566	            <!-- Categories -->
  1567	            <div class="footer-section">
  1568	                <h3>カテゴリ</h3>
  1569	                <div class="footer-links">
  1570	                    <a href="#gourmet">グルメ</a>
  1571	                    <a href="#lifestyle">ライフスタイル</a>
  1572	                    <a href="#business">ビジネス</a>
  1573	                    <a href="#culture">カルチャー</a>
  1574	                    <a href="#community">コミュニティ</a>
  1575	                    <a href="#working-holiday">ワーホリ・留学</a>
  1576	                    <a href="#health-beauty">健康・美容</a>
  1577	                    <a href="#travel">トラベル</a>
  1578	                </div>
  1579	            </div>
  1580	
  1581	            <!-- Information -->
  1582	            <div class="footer-section">
  1583	                <h3>インフォメーション</h3>
  1584	                <div class="footer-links">
  1585	                    <a href="#about">SAMPAについて</a>
  1586	                    <a href="#contact">お問い合わせ</a>
  1587	                    <a href="#columnists">コラムニスト</a>
  1588	                    <a href="#advertising">広告掲載について</a>
  1589	                    <a href="#privacy">プライバシーポリシー</a>
  1590	                    <a href="#terms">利用規約</a>
  1591	                </div>
  1592	            </div>
  1593	
  1594	            <!-- Contact Info -->
  1595	            <div class="footer-section">
  1596	                <h3>お問い合わせ先</h3>
  1597	                <div class="footer-links">
  1598	                    <p><i class="fas fa-map-marker-alt"></i> Av. Paulista, 1000<br>São Paulo - SP, Brasil</p>
  1599	                    <p><i class="fas fa-envelope"></i> info@sampa-mag.com</p>
  1600	                    <p><i class="fas fa-phone"></i> +55 11 1234-5678</p>
  1601	                </div>
  1602	            </div>
  1603	        </div>
  1604	
  1605	        <div class="footer-bottom">
  1606	            <p>&copy; 2025 SAMPA - São Paulo × Japan Magazine. All Rights Reserved.</p>
  1607	        </div>
  1608	    </footer>
  1609	
  1610	    <!-- JavaScript -->
  1611	    <script>
  1612	        // Mobile Menu Toggle
  1613	        function toggleMenu() {
  1614	            const navMenu = document.getElementById('navMenu');
  1615	            navMenu.classList.toggle('active');
  1616	        }
  1617	
  1618	        // Search Function
  1619	        function performSearch() {
  1620	            const searchInput = document.getElementById('searchInput');
  1621	            const searchTerm = searchInput.value.toLowerCase().trim();
  1622	            
  1623	            if (searchTerm === '') {
  1624	                alert('検索キーワードを入力してください。');
  1625	                return;
  1626	            }
  1627	            
  1628	            const articles = document.querySelectorAll('.article-card');
  1629	            let found = false;
  1630	            
  1631	            articles.forEach(article => {
  1632	                const title = article.querySelector('.article-title').textContent.toLowerCase();
  1633	                const excerpt = article.querySelector('.article-excerpt').textContent.toLowerCase();
  1634	                
  1635	                if (title.includes(searchTerm) || excerpt.includes(searchTerm)) {
  1636	                    article.style.display = 'flex';
  1637	                    found = true;
  1638	                } else {
  1639	                    article.style.display = 'none';
  1640	                }
  1641	            });
  1642	            
  1643	            if (!found) {
  1644	                alert(`「${searchTerm}」に一致する記事が見つかりませんでした。`);
  1645	                // Reset display
  1646	                articles.forEach(article => {
  1647	                    article.style.display = 'flex';
  1648	                });
  1649	            }
  1650	        }
  1651	
  1652	        // Search on Enter key
  1653	        document.getElementById('searchInput').addEventListener('keypress', function(e) {
  1654	            if (e.key === 'Enter') {
  1655	                performSearch();
  1656	            }
  1657	        });
  1658	
  1659	        // Contact Form Submission
  1660	        document.getElementById('contactForm').addEventListener('submit', function(e) {
  1661	            e.preventDefault();
  1662	            alert('お問い合わせありがとうございます！\n内容を確認の上、担当者よりご連絡させていただきます。');
  1663	            this.reset();
  1664	        });
  1665	
  1666	        // Smooth Scroll for anchor links
  1667	        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  1668	            anchor.addEventListener('click', function (e) {
  1669	                const href = this.getAttribute('href');
  1670	                if (href !== '#' && document.querySelector(href)) {
  1671	                    e.preventDefault();
  1672	                    document.querySelector(href).scrollIntoView({
  1673	                        behavior: 'smooth'
  1674	                    });
  1675	                }
  1676	            });
  1677	        });
  1678	
  1679	        // Close mobile menu when clicking outside
  1680	        document.addEventListener('click', function(e) {
  1681	            const navMenu = document.getElementById('navMenu');
  1682	            const mobileToggle = document.querySelector('.mobile-toggle');
  1683	            
  1684	            if (navMenu.classList.contains('active') && 
  1685	                !navMenu.contains(e.target) && 
  1686	                !mobileToggle.contains(e.target)) {
  1687	                navMenu.classList.remove('active');
  1688	            }
  1689	        });
  1690	    </script>
  1691	</body>
  1692	</html>
