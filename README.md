<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <title>Kế hoạch tuần</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 30px;
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #eef2ff, #f8fafc);
      color: #1f2937;
    }

    h1 {
      text-align: center;
      margin-bottom: 25px;
      font-size: 28px;
      font-weight: 700;
      letter-spacing: 1px;
    }

    .table-wrapper {
      background: #ffffff;
      border-radius: 16px;
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.08);
      overflow: hidden;
    }

    table {
      width: 100%;
      border-collapse: collapse;
    }

    thead th {
      background: linear-gradient(90deg, #2563eb, #4f46e5);
      color: #ffffff;
      padding: 14px 10px;
      font-size: 14px;
      text-transform: uppercase;
    }

    tbody td {
      padding: 10px;
      border-bottom: 1px solid #e5e7eb;
      vertical-align: middle;
    }

    tbody tr:last-child td {
      border-bottom: none;
    }

    .thu {
      font-weight: 700;
      text-align: center;
      background: #f1f5f9;
      width: 90px;
    }

    .sang {
      background: #ecfeff;
    }

    .chieu {
      background: #fff7ed;
    }

    input, textarea {
      resize: vertical;
      min-height: 80px;
      width: 100%;
      padding: 10px 12px;
      border-radius: 10px;
      border: 1px solid #d1d5db;
      font-size: 13px;
      line-height: 1.4;
    }

    textarea {
      resize: none;
      height: 36px;
    }

    input:focus, textarea:focus {
      outline: none;
      border-color: #4f46e5;
      box-shadow: 0 0 0 2px rgba(79, 70, 229, 0.2);
    }

    tbody tr:hover {
      background: #f8fafc;
    }

    @media (max-width: 900px) {
      body {
        padding: 15px;
      }

      h1 {
        font-size: 22px;
      }

      thead th {
        font-size: 12px;
      }
    }
  </style>
</head>
<body>

<h1>BẢNG KẾ HOẠCH LÀM VIỆC TUẦN</h1>

<div class="table-wrapper">
  <table>
    <thead>
      <tr>
        <th>Thứ</th>
        <th>Buổi sáng</th>
        <th>Tên</th>
        <th>Ghi chú</th>
        <th>Buổi chiều</th>
        <th>Tên</th>
        <th>Ghi chú</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td class="thu">Thứ 2</td>
        <td class="sang"><input placeholder="Công việc" /></td>
        <td><input placeholder="Tên" /></td>
        <td><textarea placeholder="Ghi chú"></textarea></td>
        <td class="chieu"><input placeholder="Công việc" /></td>
        <td><input placeholder="Tên" /></td>
        <td><textarea placeholder="Ghi chú"></textarea></td>
      </tr>
      <tr>
        <td class="thu">Thứ 3</td>
        <td class="sang"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
        <td class="chieu"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
      </tr>
      <tr>
        <td class="thu">Thứ 4</td>
        <td class="sang"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
        <td class="chieu"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
      </tr>
      <tr>
        <td class="thu">Thứ 5</td>
        <td class="sang"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
        <td class="chieu"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
      </tr>
      <tr>
        <td class="thu">Thứ 6</td>
        <td class="sang"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
        <td class="chieu"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
      </tr>
      <tr>
        <td class="thu">Thứ 7</td>
        <td class="sang"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
        <td class="chieu"><input /></td>
        <td><input /></td>
        <td><textarea></textarea></td>
      </tr>
    </tbody>
  </table>
</div>

<script>
  // Lưu dữ liệu tạm thời bằng LocalStorage
  const inputs = document.querySelectorAll('input, textarea');

  inputs.forEach((el, index) => {
    const savedValue = localStorage.getItem('kehoach_' + index);
    if (savedValue) el.value = savedValue;

    el.addEventListener('input', () => {
      localStorage.setItem('kehoach_' + index, el.value);
    });
  });
</script>

</body>
</html>
