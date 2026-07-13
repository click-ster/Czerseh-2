<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>サーカッド語 公式サイト</title>
    <!-- Tailwind CSS を読み込み -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        // 国旗の3色
                        flagRed: '#dc2626',   // 赤 (Red-600)
                        flagBlue: '#1d4ed8',  // 青 (Blue-700)
                        flagGreen: '#15803d', // 緑 (Green-700)
                    }
                }
            }
        }
    </script>
    <style>
        html {
            scroll-behavior: smooth;
        }
        /* 斜め国旗デザインの装飾用 */
        .diagonal-flag {
            background: linear-gradient(135deg, #dc2626 0%, #dc2626 33.3%, #1d4ed8 33.3%, #1d4ed8 66.6%, #15803d 66.6%, #15803d 100%);
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 font-sans antialiased flex flex-col min-h-screen">

    <!-- ナビゲーションバー -->
    <nav class="bg-white shadow-sm fixed w-full z-30 top-0 border-b border-gray-100">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16 items-center">
                <!-- ロゴと斜め3色国旗アイコン -->
                <div class="flex items-center space-x-3 cursor-pointer" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">
                    <!-- 斜めデザインを表現したミニ国旗 -->
                    <div class="w-8 h-6 border border-gray-200 rounded-sm overflow-hidden shadow-sm diagonal-flag"></div>
                    <span class="text-xl font-bold text-gray-900 tracking-wider">Czerseh</span>
                </div>
                <!-- ナビゲーションリンク -->
                <div class="flex space-x-4 sm:space-x-8 items-center">
                    <a href="#about" class="text-gray-600 hover:text-flagBlue px-2 py-2 text-sm font-medium transition">サーカッド語とは</a>
                    <!-- タップしたら直接 zpdic 辞書が開くようにリンク先を設定 -->
                    <a href="https://zpdic.ziphil.com/dictionary/ziCzergeh?text=&mode=both&type=prefix&orderMode=unicode&orderDirection=ascending&ignoreCase=false&enableSuggestions=true&page=0" 
                       target="_blank" 
                       rel="noopener noreferrer" 
                       class="text-gray-600 hover:text-flagBlue px-2 py-2 text-sm font-medium transition flex items-center gap-1">
                        <span>辞書 (zpdic)</span>
                        <svg class="w-3.5 h-3.5 opacity-60" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"></path></svg>
                    </a>
                    <a href="#news" class="text-gray-600 hover:text-flagBlue px-2 py-2 text-sm font-medium transition">お知らせ</a>
                    <button onclick="toggleAdminPanel()" class="text-xs bg-gray-100 hover:bg-gray-200 text-gray-600 px-2.5 py-1.5 rounded transition">
                        管理者ツール
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- ヒーローセクション -->
    <main class="flex-grow pt-16">
        <section class="bg-white border-b border-gray-100 py-20 md:py-32 relative overflow-hidden">
            <div class="max-w-4xl mx-auto px-4 text-center relative z-10">
                <!-- 国旗をモチーフにしたシンプルな3色ドット -->
                <div class="flex justify-center space-x-2 mb-6">
                    <div class="w-3 h-3 bg-flagRed rounded-full shadow-sm"></div>
                    <div class="w-3 h-3 bg-flagBlue rounded-full shadow-sm"></div>
                    <div class="w-3 h-3 bg-flagGreen rounded-full shadow-sm"></div>
                </div>
                
                <h1 class="text-5xl md:text-7xl font-extrabold text-gray-900 tracking-tight mb-4">
                    Czerseh
                </h1>
                <p class="text-lg md:text-2xl text-gray-500 font-medium tracking-wide mb-8">
                    サーカッド語公式サイト
                </p>
                <p class="max-w-2xl mx-auto text-base md:text-lg text-gray-600 leading-relaxed mb-10">
                   このサイトは独自の世界観と言語体系を持つ,サーカッド語の世界を発信するウェブサイトです
                </p>
                <div class="flex justify-center space-x-4">
                    <a href="#about" class="bg-flagBlue hover:bg-blue-800 text-white font-bold px-6 py-3 rounded-md shadow transition">
                        この言語の概要
                    </a>
                    <a href="https://zpdic.ziphil.com/dictionary/ziCzergeh?text=&mode=both&type=prefix&orderMode=unicode&orderDirection=ascending&ignoreCase=false&enableSuggestions=true&page=0" 
                       target="_blank" 
                       rel="noopener noreferrer" 
                       class="bg-gray-100 hover:bg-gray-200 text-gray-800 font-bold px-6 py-3 rounded-md transition">
                        zpdic 辞書を開く
                    </a>
                </div>
            </div>
        </section>

        <!-- サーカッド語について (紹介セクション) -->
        <section id="about" class="py-16 bg-gray-50">
            <div class="max-w-4xl mx-auto px-4">
                <div class="bg-white p-8 md:p-12 rounded-xl shadow-sm border border-gray-100">
                    <h2 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6 flex items-center">
                        <span class="w-2 h-8 bg-flagGreen rounded-full mr-3"></span>
                        サーカッド語について
                    </h2>
                    
                    <div class="space-y-6 text-gray-600 leading-relaxed">
                        <p>
                            サーカッド語は,ヨーロッパにあるサーカッド共和国で話される独自の言語です.
                        </p>
                        <p>
                            サーカッド語は多くの格や他のヨーロッパ言語と異なる独特の文法体系を持ち,難解な言語とされます.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 記事・お知らせセクション -->
        <section id="news" class="py-16 bg-gray-50 border-t border-gray-100">
            <div class="max-w-4xl mx-auto px-4">
                <h2 class="text-2xl md:text-3xl font-bold text-gray-900 mb-8 flex items-center">
                    <span class="w-2 h-8 bg-flagRed rounded-full mr-3"></span>
                    更新情報・お知らせ
                </h2>
                
                <!-- 投稿された記事が入る場所 -->
                <div id="article-list" class="space-y-6">
                    <!-- 初期状態（記事がない場合や、ロード中の表示） -->
                    <p id="no-articles-msg" class="text-gray-400 italic">お知らせはまだありません。管理者ツールから投稿できます。</p>
                </div>
            </div>
        </section>
    </main>

    <!-- 管理者ツール用の設定パネル（デフォルト非表示） -->
    <div id="admin-panel" class="fixed inset-0 z-40 bg-gray-900/50 backdrop-blur-sm flex items-center justify-center hidden p-4">
        <div class="bg-white w-full max-w-lg rounded-xl shadow-2xl p-6 border border-gray-100 max-h-[90vh] flex flex-col">
            <div class="flex justify-between items-center pb-4 border-b border-gray-100">
                <h3 class="text-lg font-bold text-gray-900 flex items-center">
                    <span class="w-3 h-3 bg-flagBlue rounded-full mr-2"></span>
                    管理者用 記事作成ツール
                </h3>
                <button onclick="toggleAdminPanel()" class="text-gray-400 hover:text-gray-600 text-xl font-bold">✕</button>
            </div>
            
            <!-- 投稿フォーム -->
            <div class="py-4 space-y-4 overflow-y-auto flex-grow">
                <!-- エラーメッセージ表示欄 -->
                <div id="admin-error-msg" class="hidden text-red-600 bg-red-50 p-3 rounded-md text-xs font-bold border border-red-100"></div>
                
                <div>
                    <label for="post-title" class="block text-xs font-bold text-gray-500 uppercase mb-1">記事のタイトル</label>
                    <input type="text" id="post-title" placeholder="文法を追加しました、等" class="w-full px-3 py-2 border border-gray-200 rounded-md focus:outline-none focus:ring-2 focus:ring-flagBlue text-sm">
                </div>
                <div>
                    <label for="post-content" class="block text-xs font-bold text-gray-500 uppercase mb-1">記事の内容</label>
                    <textarea id="post-content" placeholder="ここにお知らせの本文を書きます。改行もそのまま反映されます。" rows="5" class="w-full px-3 py-2 border border-gray-200 rounded-md focus:outline-none focus:ring-2 focus:ring-flagBlue text-sm"></textarea>
                </div>
                <button onclick="publishArticle()" class="w-full bg-flagGreen hover:bg-green-800 text-white font-bold py-2.5 rounded-md shadow transition text-sm">
                    記事を公開する
                </button>
            </div>

            <!-- 削除リスト -->
            <div class="border-t border-gray-100 pt-4 flex flex-col min-h-0">
                <h4 class="text-xs font-bold text-gray-400 uppercase mb-2">公開中の記事一覧 (削除可能)</h4>
                <div id="admin-article-list" class="space-y-2 overflow-y-auto text-xs flex-grow max-h-40">
                    <!-- ここに削除用リストが並びます -->
                </div>
            </div>
        </div>
    </div>

    <!-- フッター -->
    <footer class="bg-gray-900 text-gray-400 py-12 px-4">
        <div class="max-w-4xl mx-auto flex flex-col md:flex-row justify-between items-center">
            <div class="mb-4 md:mb-0">
                <span class="text-white font-bold text-lg tracking-wider">サーカッド語</span>
                <p class="text-xs text-gray-500 mt-1">&copy; 2026 Sarkad Project. All rights reserved.</p>
            </div>
            <div class="flex space-x-6 text-xs">
                <a href="#about" class="hover:text-white transition">About</a>
                <!-- フッター側も zpdic 辞書が開くように設定 -->
                <a href="https://zpdic.ziphil.com/dictionary/ziCzergeh?text=&mode=both&type=prefix&orderMode=unicode&orderDirection=ascending&ignoreCase=false&enableSuggestions=true&page=0" 
                   target="_blank" 
                   rel="noopener noreferrer" 
                   class="hover:text-white transition">Dictionary</a>
                <a href="#news" class="hover:text-white transition">News</a>
            </div>
        </div>
    </footer>

    <!-- Firebase SDK (ES modules) を使用してオンライン保存処理を実装 -->
    <script type="module">
        // ==========================================
        // 🛠️ 【世界公開用のFirebase設定欄】
        // ==========================================
        // Firebaseにプロジェクトを作成したら、コンソールで発行される設定オブジェクトをここに貼り付けてください。
        // 設定を貼り付けると、自動的に世界共有のクラウド保存モードに切り替わります！
        const myFirebaseConfig = {
            apiKey: "ここにあなたのAPIキーを貼ってください",
            authDomain: "あなたのプロジェクト.firebaseapp.com",
            projectId: "あなたのプロジェクトID",
            storageBucket: "あなたのプロジェクト.appspot.com",
            messagingSenderId: "あなたのメッセージID",
            appId: "あなたのアプリID"
        };
        // ==========================================

        let db = null;
        let auth = null;
        let isCloudMode = false;

        // Firebaseが正しく設定されているか自動判定する関数
        function checkFirebaseConfig(config) {
            return config && config.apiKey && !config.apiKey.includes("ここにあなたの");
        }

        // アプリ起動時の初期化
        async function startApp() {
            // あなた自身の個別設定がある場合、または環境からFirebase設定が渡されている場合
            const hasEnvConfig = typeof __firebase_config !== 'undefined' && __firebase_config;
            let activeConfig = null;

            if (checkFirebaseConfig(myFirebaseConfig)) {
                activeConfig = myFirebaseConfig;
                isCloudMode = true;
            } else if (hasEnvConfig) {
                activeConfig = JSON.parse(__firebase_config);
                isCloudMode = true;
            }

            if (isCloudMode && activeConfig) {
                // クラウド保存（Firebase）モードで起動
                try {
                    const { initializeApp } = await import("https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js");
                    const { getAuth, signInAnonymously, onAuthStateChanged } = await import("https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js");
                    const { getFirestore, collection, addDoc, deleteDoc, doc, onSnapshot } = await import("https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js");

                    const app = initializeApp(activeConfig);
                    auth = getAuth(app);
                    db = getFirestore(app);

                    await signInAnonymously(auth);

                    onAuthStateChanged(auth, (user) => {
                        if (user) {
                            subscribeNewsFirebase(collection, onSnapshot);
                        }
                    });
                } catch (error) {
                    console.error("クラウド接続エラー。ローカル保存に切り替えます:", error);
                    isCloudMode = false;
                    startLocalMode();
                }
            } else {
                // ローカル保存モードで起動（プレビュー画面やPCのダブルクリック確認用）
                startLocalMode();
            }
        }

        // --- Firebaseモードの時の処理 ---
        function subscribeNewsFirebase(collection, onSnapshot) {
            const appId = typeof __app_id !== 'undefined' ? __app_id : 'czerseh-lang';
            const newsCollectionRef = collection(db, 'artifacts', appId, 'public', 'data', 'news_posts');

            onSnapshot(newsCollectionRef, (snapshot) => {
                const articles = [];
                snapshot.forEach((doc) => {
                    const data = doc.data();
                    articles.push({
                        id: doc.id,
                        title: data.title || '',
                        content: data.content || '',
                        timestamp: data.timestamp || 0
                    });
                });
                renderArticles(articles);
            }, (error) => {
                console.error("クラウド同期エラー:", error);
                startLocalMode();
            });
        }

        // --- ローカル保存モードの時の処理 ---
        function startLocalMode() {
            isCloudMode = false;
            renderArticles(getLocalArticles());
        }

        function getLocalArticles() {
            const data = localStorage.getItem('czerseh_news_posts_local');
            return data ? JSON.parse(data) : [];
        }

        function saveLocalArticles(articles) {
            localStorage.setItem('czerseh_news_posts_local', JSON.stringify(articles));
            renderArticles(articles);
        }

        // --- 共通：描画処理 ---
        function renderArticles(articles) {
            const articleListContainer = document.getElementById('article-list');
            const adminArticleListContainer = document.getElementById('admin-article-list');
            const noMsg = document.getElementById('no-articles-msg');

            articleListContainer.innerHTML = '';
            adminArticleListContainer.innerHTML = '';

            if (!articles || articles.length === 0) {
                articleListContainer.appendChild(noMsg);
                noMsg.style.display = 'block';
                noMsg.innerText = 'お知らせはまだありません。管理者ツールから投稿できます。';
                adminArticleListContainer.innerHTML = '<p class="text-gray-400 italic">投稿された記事はありません。</p>';
                return;
            } else {
                noMsg.style.display = 'none';
            }

            // 新しい日付順にソート
            articles.sort((a, b) => b.timestamp - a.timestamp);

            articles.forEach((art) => {
                const dateString = new Date(art.timestamp).toLocaleDateString('ja-JP', {
                    year: 'numeric', month: '2-digit', day: '2-digit'
                });

                // 一般公開ページ側の表示
                const card = document.createElement('div');
                card.className = "bg-white p-6 rounded-lg shadow-sm border border-gray-100 hover:shadow-md transition";
                card.innerHTML = `
                    <div class="flex items-center space-x-2 text-xs text-gray-400 mb-2">
                        <span class="w-2 h-2 bg-flagBlue rounded-full"></span>
                        <time>${dateString}</time>
                    </div>
                    <h3 class="text-lg font-bold text-gray-900 mb-3">${escapeHtml(art.title)}</h3>
                    <p class="text-gray-600 text-sm whitespace-pre-wrap leading-relaxed">${escapeHtml(art.content)}</p>
                `;
                articleListContainer.appendChild(card);

                // 管理者用削除リスト（二段階削除ボタン）
                const adminItem = document.createElement('div');
                adminItem.className = "flex justify-between items-center bg-gray-50 p-2 rounded border border-gray-100";
                
                // ID内の特殊文字を回避するため安全な文字列にエスケープして属性に渡す
                const safeId = typeof art.id === 'string' ? art.id.replace(/[^a-zA-Z0-9]/g, '_') : art.id;

                adminItem.innerHTML = `
                    <span class="truncate font-medium text-gray-700 max-w-[180px]">${escapeHtml(art.title)}</span>
                    <div class="flex items-center space-x-1">
                        <button id="del-btn-${safeId}" onclick="confirmDelete('${safeId}')" class="text-red-500 hover:text-red-700 font-bold px-2 py-1">削除</button>
                        <button id="confirm-btn-${safeId}" onclick="executeDelete('${art.id}', '${safeId}')" class="hidden bg-red-600 hover:bg-red-700 text-white font-bold px-2 py-1 rounded">本当に削除？</button>
                        <button id="cancel-btn-${safeId}" onclick="cancelDelete('${safeId}')" class="hidden text-gray-500 hover:text-gray-700 px-2 py-1">戻る</button>
                    </div>
                `;
                adminArticleListContainer.appendChild(adminItem);
            });
        }

        // --- 共通：記事を追加する処理 ---
        async function publishArticle() {
            const titleInput = document.getElementById('post-title');
            const contentInput = document.getElementById('post-content');
            const errorMsg = document.getElementById('admin-error-msg');

            const title = titleInput.value.trim();
            const content = contentInput.value.trim();

            if (!title || !content) {
                errorMsg.innerText = 'タイトルと内容を両方入力してください。';
                errorMsg.classList.remove('hidden');
                return;
            }

            errorMsg.classList.add('hidden');

            const timestamp = Date.now();

            if (isCloudMode) {
                // クラウド保存処理
                try {
                    const { collection, addDoc } = window.firebaseFirestore;
                    const appId = typeof __app_id !== 'undefined' ? __app_id : 'czerseh-lang';
                    const newsCollectionRef = collection(db, 'artifacts', appId, 'public', 'data', 'news_posts');
                    await addDoc(newsCollectionRef, { title, content, timestamp });
                } catch (error) {
                    console.error("クラウド保存失敗:", error);
                    errorMsg.innerText = 'クラウドへの保存に失敗しました。';
                    errorMsg.classList.remove('hidden');
                    return;
                }
            } else {
                // ローカル保存処理
                const articles = getLocalArticles();
                articles.unshift({ id: Date.now(), title, content, timestamp });
                saveLocalArticles(articles);
            }

            titleInput.value = '';
            contentInput.value = '';
            toggleAdminPanel();
        }

        // --- 共通：記事を削除する処理 ---
        async function executeDelete(originalId, safeId) {
            const errorMsg = document.getElementById('admin-error-msg');
            if (isCloudMode) {
                // クラウド削除処理
                try {
                    const { doc, deleteDoc } = window.firebaseFirestore;
                    const appId = typeof __app_id !== 'undefined' ? __app_id : 'czerseh-lang';
                    const docRef = doc(db, 'artifacts', appId, 'public', 'data', 'news_posts', originalId);
                    await deleteDoc(docRef);
                } catch (error) {
                    console.error("クラウド削除失敗:", error);
                    if (errorMsg) {
                        errorMsg.innerText = '削除に失敗しました。';
                        errorMsg.classList.remove('hidden');
                    }
                }
            } else {
                // ローカル削除処理
                let articles = getLocalArticles();
                const numericId = Number(originalId);
                articles = articles.filter(art => {
                    if (isNaN(numericId)) {
                        return art.id !== originalId;
                    }
                    return art.id !== numericId && art.id !== originalId;
                });
                saveLocalArticles(articles);
            }
        }

        // ボタンの2段階表示制御
        function confirmDelete(id) {
            document.getElementById(`del-btn-${id}`).classList.add('hidden');
            document.getElementById(`confirm-btn-${id}`).classList.remove('hidden');
            document.getElementById(`cancel-btn-${id}`).classList.remove('hidden');
        }

        function cancelDelete(id) {
            document.getElementById(`del-btn-${id}`).classList.remove('hidden');
            document.getElementById(`confirm-btn-${id}`).classList.add('hidden');
            document.getElementById(`cancel-btn-${id}`).classList.add('hidden');
        }

        function toggleAdminPanel() {
            const panel = document.getElementById('admin-panel');
            panel.classList.toggle('hidden');
            document.getElementById('admin-error-msg').classList.add('hidden');
        }

        function escapeHtml(str) {
            return str
                .replace(/&/g, "&amp;")
                .replace(/</g, "&lt;")
                .replace(/>/g, "&gt;")
                .replace(/"/g, "&quot;")
                .replace(/'/g, "&#039;");
        }

        // 関数のグローバル展開
        window.publishArticle = publishArticle;
        window.confirmDelete = confirmDelete;
        window.cancelDelete = cancelDelete;
        window.executeDelete = executeDelete;
        window.toggleAdminPanel = toggleAdminPanel;

        startApp();
    </script>
</body>
</html>
