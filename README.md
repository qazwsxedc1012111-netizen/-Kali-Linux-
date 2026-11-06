<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>أوامر ترمينال Kali Linux وأفضل الأدوات</title>
    <style>
        :root {
            --bg-color: #0d1117;
            --card-bg: #161b22;
            --accent-color: #2f81f7;
            --terminal-green: #39d353;
            --text-color: #c9d1d9;
            --border-color: #30363d;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            padding: 30px 20px;
            background-color: var(--card-bg);
            border-radius: 12px;
            border: 1px solid var(--border-color);
            margin-bottom: 25px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
        }

        header h1 {
            color: #ffffff;
            margin-bottom: 15px;
            font-size: 1.8rem;
        }

        .banner-img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            border: 1px solid var(--border-color);
            max-height: 250px;
            object-fit: cover;
        }

        .table-wrapper {
            background-color: var(--card-bg);
            border-radius: 12px;
            border: 1px solid var(--border-color);
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
        }

        table {
            width: 100%;
            border-collapse: collapse;
            text-align: right;
        }

        th, td {
            padding: 14px 18px;
            border-bottom: 1px solid var(--border-color);
        }

        th {
            background-color: #21262d;
            color: #ffffff;
            font-size: 1.05rem;
        }

        tr:hover {
            background-color: #1c2129;
        }

        code {
            font-family: 'Courier New', Courier, monospace;
            background-color: #000000;
            color: var(--terminal-green);
            padding: 4px 8px;
            border-radius: 5px;
            font-weight: bold;
            display: inline-block;
            direction: ltr;
        }

        .cmd-name {
            font-weight: bold;
            color: var(--accent-color);
        }

        footer {
            text-align: center;
            margin-top: 30px;
            color: #8b949e;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <div class="container">
        <header>
            <h1>أوامر Terminal الأساسية في Kali Linux وأفضل الأدوات</h1>
            <img class="banner-img" src="https://images.unsplash.com/photo-1629654297299-c8506221ca97?auto=format&fit=crop&w=800&q=80" alt="Linux Terminal Header">
        </header>

        <div class="table-wrapper">
            <table>
                <thead>
                    <tr>
                        <th>الأمر</th>
                        <th>طريقة الاستخدام</th>
                        <th>الفائدة / الوظيفة</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="cmd-name">pwd</td>
                        <td><code>pwd</code></td>
                        <td>معرفة مسار المجلد الحالي الذي تقف فيه داخل النظام.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">ls -la</td>
                        <td><code>ls -la</code></td>
                        <td>عرض كافة الملفات والمجلدات (بما فيها المخفية) بتفاصيل الصلاحيات والأحجام.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">cd</td>
                        <td><code>cd /path/to/dir</code> أو <code>cd ..</code></td>
                        <td>التنقل بين المجلدات أو الرجوع للمجلد السابق.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">mkdir</td>
                        <td><code>mkdir folder_name</code></td>
                        <td>إنشاء مجلد جديد.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">touch</td>
                        <td><code>touch file.txt</code></td>
                        <td>إنشاء ملف نصي فارغ جديد.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">cp</td>
                        <td><code>cp source_file destination</code></td>
                        <td>نسخ ملف أو مجلد إلى مكان آخر.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">mv</td>
                        <td><code>mv old_name new_name</code></td>
                        <td>نقل الملفات من مكان لآخر أو إعادة تسميتها.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">rm -rf</td>
                        <td><code>rm -rf target_name</code></td>
                        <td>حذف الملفات أو المجلدات ومحتوياتها نهائياً.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">sudo</td>
                        <td><code>sudo command</code></td>
                        <td>تنفيذ الأوامر بصلاحيات المدير (Root).</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">apt update</td>
                        <td><code>sudo apt update && sudo apt upgrade -y</code></td>
                        <td>تحديث قائمة المستودعات وتطوير كافة حزم النظام المثبتة لأحدث إصدار.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">apt install</td>
                        <td><code>sudo apt install package_name -y</code></td>
                        <td>تحميل وتثبيت البرامج والأدوات الجديدة.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">chmod +x</td>
                        <td><code>chmod +x script.sh</code></td>
                        <td>منح الملف أو السكربت صلاحية التشغيل كبرنامج تنفيذي.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">ip a</td>
                        <td><code>ip a</code></td>
                        <td>عرض كروت الشبكة وعناوين الـ IP الخاصة بالجهاز.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">nmap</td>
                        <td><code>nmap -sn 192.168.1.0/24</code></td>
                        <td>فحص الشبكة المحلية واكتشاف جميع الأجهزة النشطة والمتصلة بها.</td>
                    </tr>
                    <tr>
                        <td class="cmd-name">arp -a</td>
                        <td><code>arp -a</code></td>
                        <td>عرض جدول الـ ARP لمعرفة عناوين الـ MAC للأجهزة المتصلة على الشبكة.</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <footer>
            <p>دليل أوامر Kali Linux الأساسية</p>
        </footer>
    </div>

</body>
</html>
دليل لاوامر    linux
