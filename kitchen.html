<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chaat Puchka - Kitchen KDS</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-slate-950 text-white font-sans p-4 sm:p-6">
    <div class="max-w-6xl mx-auto">
        <div class="flex flex-col sm:flex-row justify-between items-center gap-4 mb-6 bg-slate-900 p-5 rounded-2xl border border-slate-800 shadow-md">
            <div class="flex items-center space-x-3 w-full sm:w-auto">
                <div class="w-12 h-12 flex-shrink-0 bg-black rounded-xl p-1 shadow border border-slate-800 flex items-center justify-center">
                    <img src="https://i.postimg.cc/SsSZBQ9q/1000037254-removebg-preview.png" alt="Logo" class="w-full h-full object-contain">
                </div>
                <h2 id="kds-title" class="text-xl sm:text-2xl font-black text-white tracking-tight">Kitchen KDS</h2>
            </div>
            <button onclick="window.location.href='kitchen-login.html'" class="bg-red-500 hover:bg-red-600 px-4 py-2 rounded-xl font-semibold text-sm shadow transition w-full sm:w-auto">Logout</button>
        </div>
        <div id="orders-container" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
            <p class="text-slate-400">Loading live kitchen orders...</p>
        </div>
    </div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
        import { getDatabase, ref, onValue, update } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-database.js";

        const firebaseConfig = {
            databaseURL: "https://teat-2-4b868-default-rtdb.europe-west1.firebasedatabase.app/"
        };
        const app = initializeApp(firebaseConfig);
        const db = getDatabase(app);

        const urlParams = new URLSearchParams(window.location.search);
        const branchId = urlParams.get('branchId');
        const branchName = decodeURIComponent(urlParams.get('branchName') || 'Kitchen');

        if (!branchId) {
            window.location.href = 'kitchen-login.html';
        }

        document.getElementById('kds-title').innerText = `Kitchen KDS - ${branchName}`;

        onValue(ref(db, `orders/${branchId}`), (snapshot) => {
            const data = snapshot.val();
            const container = document.getElementById('orders-container');
            container.innerHTML = '';

            if (!data) {
                container.innerHTML = '<p class="text-slate-400">No active kitchen orders.</p>';
                return;
            }

            Object.entries(data).forEach(([id, order]) => {
                let itemsList = order.items.map(i => `<li>${i.name} (x${i.qty || 1})</li>`).join('');
                container.innerHTML += `
                    <div class="bg-slate-900 p-5 rounded-2xl border border-slate-800 shadow-md flex flex-col justify-between">
                        <div>
                            <div class="flex justify-between font-bold mb-3 text-base">
                                <span>Order #${id.slice(-4)}</span>
                                <span class="bg-emerald-500/20 text-emerald-400 text-xs px-3 py-1 rounded-full font-bold">${order.status}</span>
                            </div>
                            <ul class="text-sm text-slate-300 list-disc pl-5 mb-4 space-y-1">${itemsList}</ul>
                            <p class="text-xs text-slate-400 mb-4 bg-slate-950 p-3 rounded-xl border border-slate-800"><strong>Address:</strong> ${order.address}</p>
                        </div>
                        <button onclick="updateStatus('${id}', 'Completed')" class="w-full bg-emerald-600 hover:bg-emerald-700 py-3 rounded-xl text-sm font-black shadow transition">Mark Completed</button>
                    </div>`;
            });
        });

        window.updateStatus = function(orderId, newStatus) {
            update(ref(db, `orders/${branchId}/${orderId}`), { status: newStatus });
        };
    </script>
</body>
</html>
