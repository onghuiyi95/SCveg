import React, { useState, useMemo, useEffect } from 'react';
import { Search, Plus, Minus, Printer, MapPin, Receipt, FileText, Settings2 } from 'lucide-react';

// 根据你最新的本地化习惯(马来文/拼音/英文混合)更新的商品库
const initialProducts = [
  // 叶菜类
  { id: '1', enName: 'Mani cai', cnName: '带枝玛尼菜', unit: 'kg', category: '叶菜类' },
  { id: '2', enName: 'Plucked manicai', cnName: '摘好玛尼菜', unit: 'kg', category: '叶菜类' },
  { id: '3', enName: 'Sawi jepun', cnName: '小白菜', unit: 'kg', category: '叶菜类' },
  { id: '4', enName: 'Spinach', cnName: '菠菜', unit: 'kg', category: '叶菜类' },
  { id: '5', enName: 'Beijing', cnName: '北京包菜', unit: 'kg', category: '叶菜类' },
  { id: '6', enName: 'Long cabbage', cnName: '大白菜/长白菜', unit: 'nos', category: '叶菜类' },
  { id: '7', enName: 'Green coral', cnName: '生菜', unit: 'kg', category: '叶菜类' },
  { id: '8', enName: 'Dou miao', cnName: '有机豆苗', unit: 'g', category: '叶菜类' },
  { id: '9', enName: 'Lettuce', cnName: '普通生菜', unit: 'kg', category: '叶菜类' },
  { id: '10', enName: 'Indonesia cabbage', cnName: '印尼包菜', unit: 'nos', category: '叶菜类' },
  
  // 瓜果根茎
  { id: '11', enName: 'Long bean', cnName: '长豆', unit: 'kg', category: '瓜果根茎' },
  { id: '12', enName: 'Cucumber', cnName: '黄瓜', unit: 'kg', category: '瓜果根茎' },
  { id: '13', enName: 'Tomato', cnName: '西红柿/番茄', unit: 'kg', category: '瓜果根茎' },
  { id: '14', enName: 'Turnip', cnName: '芒光', unit: 'kg', category: '瓜果根茎' },
  { id: '15', enName: 'Pumpkin', cnName: '南瓜', unit: 'kg', category: '瓜果根茎' },
  { id: '16', enName: 'Carrot', cnName: '胡萝卜', unit: 'ctn', category: '瓜果根茎' },
  { id: '17', enName: 'Taro', cnName: '四号泰国芋头', unit: 'ctn', category: '瓜果根茎' },
  { id: '18', enName: 'Celery', cnName: '西芹', unit: 'pkt', category: '瓜果根茎' },
  { id: '19', enName: 'Sweet corn', cnName: '玉米', unit: 'pkt', category: '瓜果根茎' },
  { id: '20', enName: 'Baby corn', cnName: '玉米芯', unit: 'pkt', category: '瓜果根茎' },
  { id: '21', enName: 'Broccoli', cnName: '西兰花', unit: 'g', category: '瓜果根茎' },
  { id: '22', enName: 'Cauliflower', cnName: '白花菜', unit: 'g', category: '瓜果根茎' },
  { id: '23', enName: 'Radish', cnName: '白萝卜', unit: 'kg', category: '瓜果根茎' },
  { id: '24', enName: 'Potato', cnName: '土豆', unit: 'kg', category: '瓜果根茎' },
  { id: '25', enName: 'Brinjal', cnName: '茄子', unit: 'kg', category: '瓜果根茎' },

  // 菇类
  { id: '26', enName: 'Abalone', cnName: '灰菇/鲍鱼菇', unit: 'pkt', category: '菇类' },
  { id: '27', enName: 'King oyster', cnName: '杏鲍菇', unit: 'pkt', category: '菇类' },
  { id: '28', enName: 'Enoki', cnName: '金针菇', unit: 'pkt', category: '菇类' },
  { id: '29', enName: 'Brown shimeiji', cnName: '蟹味菇', unit: 'pkt', category: '菇类' },
  { id: '30', enName: 'Shitake', cnName: '香菇', unit: 'pkt', category: '菇类' },

  // 配料香料
  { id: '31', enName: 'Pandan leaf', cnName: '斑斓叶', unit: 'g', category: '配料/香料' },
  { id: '32', enName: 'Serai', cnName: '香茅', unit: 'kg', category: '配料/香料' },
  { id: '33', enName: 'Limau kasturi', cnName: '小酸柑', unit: 'g', category: '配料/香料' },
  { id: '34', enName: 'Coriander', cnName: '香菜 (芫茜)', unit: 'g', category: '配料/香料' },
  { id: '35', enName: 'Bentong ginger', cnName: '文东姜', unit: 'g', category: '配料/香料' },
  { id: '36', enName: 'Ginger', cnName: '生姜', unit: 'kg', category: '配料/香料' },
  { id: '37', enName: 'Lemon', cnName: '柠檬', unit: 'nos', category: '配料/香料' },
  { id: '38', enName: 'Pineapple', cnName: '黄梨', unit: 'nos', category: '配料/香料' },
  { id: '39', enName: 'Chilli padi', cnName: '小米辣', unit: 'g', category: '配料/香料' },
  { id: '40', enName: 'Curry leaf', cnName: '咖喱叶', unit: 'g', category: '配料/香料' },
];

const categories = ['全部', '叶菜类', '瓜果根茎', '菇类', '配料/香料'];

export default function PurchaseOrderV2() {
  const [products] = useState(initialProducts);
  const [searchQuery, setSearchQuery] = useState('');
  const [activeCategory, setActiveCategory] = useState('全部');
  const [cart, setCart] = useState({});
  const [remark, setRemark] = useState({});
  
  // 生成 PO 编号 (自动获取当天日期生成单号)
  const getTodayPO = () => {
    const d = new Date();
    return `PO-${d.getFullYear()}${String(d.getMonth()+1).padStart(2, '0')}${String(d.getDate()).padStart(2, '0')}-01`;
  };

  // 自动获取明天日期作为订单日期 (比如 25号操作，默认订单日期就是26号)
  const getTomorrowDate = () => {
    const tomorrow = new Date();
    tomorrow.setDate(tomorrow.getDate() + 1);
    return tomorrow.toISOString().split('T')[0];
  };

  // ======== 默认信息更新为你的真实资料 ========
  const defaultCompanyName = 'SUNNYCHOICE PTE. LTD.';
  const defaultAddress = 'Blk 630 Bukit Batok Central\n#01-154-#01-156\nSingapore 650630';
  
  const [companyName, setCompanyName] = useState(defaultCompanyName);
  const [poNumber, setPoNumber] = useState(getTodayPO());
  const [orderDate, setOrderDate] = useState(getTomorrowDate());
  
  // 账单地址和收货地址默认使用公司总地址
  const [billTo, setBillTo] = useState(defaultAddress);
  const [shipTo, setShipTo] = useState(defaultAddress);
  const [poNotes, setPoNotes] = useState('* Please separate bill.\n* Please ensure fresh quality.');

  const filteredProducts = useMemo(() => {
    return products.filter(p => {
      const matchCategory = activeCategory === '全部' || p.category === activeCategory;
      const query = searchQuery.toLowerCase();
      const matchSearch = p.enName.toLowerCase().includes(query) || p.cnName.includes(query);
      return matchCategory && matchSearch;
    });
  }, [products, searchQuery, activeCategory]);

  const selectedItems = useMemo(() => {
    return products
      .filter(p => cart[p.id] > 0)
      .map(p => ({
        ...p,
        quantity: cart[p.id],
        itemRemark: remark[p.id] || ''
      }));
  }, [cart, remark, products]);

  const increment = (id) => setCart(prev => ({ ...prev, [id]: (prev[id] || 0) + 1 }));
  const decrement = (id) => {
    setCart(prev => {
      const newQty = (prev[id] || 0) - 1;
      if (newQty <= 0) {
        const newCart = { ...prev };
        delete newCart[id];
        return newCart;
      }
      return { ...prev, [id]: newQty };
    });
  };

  const handleQuantityChange = (id, value) => {
    const num = parseFloat(value);
    if (isNaN(num) || num <= 0) {
      if (value === '') {
        setCart(prev => {
          const newCart = { ...prev };
          delete newCart[id];
          return newCart;
        });
      }
    } else {
      setCart(prev => ({ ...prev, [id]: num }));
    }
  };

  // 触发浏览器打印并生成PDF
  const handleDownloadPDF = () => {
    if (selectedItems.length === 0) {
      alert("请先选择商品！");
      return;
    }
    window.print();
  };

  return (
    <div className="min-h-screen bg-gray-100 font-sans text-gray-800 flex flex-col hide-on-print">
      
      {/* 顶部导航 */}
      <header className="bg-slate-800 text-white shadow-md sticky top-0 z-30 hide-on-print">
        <div className="max-w-[1600px] mx-auto px-4 py-3 flex justify-between items-center">
          <h1 className="text-lg md:text-xl font-bold flex items-center gap-2">
            <FileText className="w-5 h-5 md:w-6 md:h-6 text-emerald-400" />
            <span className="hidden sm:inline">PO 采购单生成系统 V2.0</span>
            <span className="inline sm:hidden">采购单 V2.0</span>
          </h1>
          <button 
            onClick={handleDownloadPDF}
            className="bg-emerald-600 hover:bg-emerald-500 text-white px-4 py-2 rounded-lg text-sm md:text-base font-medium flex items-center gap-2 transition-colors shadow-sm"
          >
            <Printer className="w-4 h-4 md:w-5 md:h-5" />
            <span className="hidden sm:inline">生成 / 下载 PDF</span>
            <span className="inline sm:hidden">打印 PDF</span>
          </button>
        </div>
      </header>

      {/* 主体内容：使用 lg:flex-row 实现宽屏左右分栏，窄屏上下堆叠 */}
      <main className="flex-1 max-w-[1600px] w-full mx-auto p-4 flex flex-col lg:flex-row gap-6 items-start">
        
        {/* ================= 左侧：控制面板 ================= */}
        {/* 在小屏幕上它会自然堆叠在最上方，大屏幕上它会吸附在左侧 */}
        <div className="w-full lg:w-[400px] xl:w-[450px] flex flex-col gap-4 hide-on-print lg:sticky lg:top-20 z-10 shrink-0">
          
          {/* 地址与信息设置 */}
          <div className="bg-white rounded-xl shadow-sm border border-gray-200 p-4">
            <h2 className="font-bold text-gray-800 flex items-center gap-2 mb-4 border-b pb-2">
              <Settings2 className="w-5 h-5 text-slate-500" /> 单据基础设置
            </h2>
            
            <div className="grid grid-cols-2 gap-3 mb-4">
              <div>
                <label className="block text-xs font-medium text-gray-500 mb-1">PO Number (单号)</label>
                <input type="text" value={poNumber} onChange={e => setPoNumber(e.target.value)} className="w-full text-sm border rounded px-3 py-1.5 focus:border-emerald-500 focus:ring-1 focus:ring-emerald-500 outline-none font-mono" />
              </div>
              <div>
                <label className="block text-xs font-medium text-gray-500 mb-1">Order Date (日期)</label>
                <input type="date" value={orderDate} onChange={e => setOrderDate(e.target.value)} className="w-full text-sm border rounded px-3 py-1.5 focus:border-emerald-500 focus:ring-1 focus:ring-emerald-500 outline-none" />
              </div>
            </div>

            <div className="space-y-3">
              <div>
                <label className="block text-xs font-medium text-gray-500 mb-1 flex items-center gap-1"><Receipt className="w-3 h-3"/> Billing Address (账单地址)</label>
                <textarea rows="3" value={billTo} onChange={e => setBillTo(e.target.value)} className="w-full text-sm border rounded px-3 py-2 focus:border-emerald-500 outline-none resize-none"></textarea>
              </div>
              <div>
                <label className="block text-xs font-medium text-gray-500 mb-1 flex items-center gap-1"><MapPin className="w-3 h-3"/> Delivery Address (送货地址)</label>
                <textarea rows="3" value={shipTo} onChange={e => setShipTo(e.target.value)} className="w-full text-sm border rounded px-3 py-2 focus:border-emerald-500 outline-none resize-none"></textarea>
              </div>
            </div>
          </div>

          {/* 商品选择器 */}
          <div className="bg-white rounded-xl shadow-sm border border-gray-200 overflow-hidden flex flex-col h-[55vh] lg:h-[calc(100vh-480px)] min-h-[400px]">
            <div className="p-3 bg-slate-50 border-b border-gray-200">
              <div className="relative mb-3">
                <Search className="w-4 h-4 absolute left-3 top-1/2 -translate-y-1/2 text-gray-400" />
                <input 
                  type="text" placeholder="搜索 (中文/英文/马来文)..." value={searchQuery} onChange={e => setSearchQuery(e.target.value)}
                  className="w-full pl-9 pr-3 py-2 text-sm rounded border border-gray-300 focus:border-emerald-500 outline-none"
                />
              </div>
              <div className="flex gap-2 overflow-x-auto pb-1 hide-scrollbar">
                {categories.map(cat => (
                  <button key={cat} onClick={() => setActiveCategory(cat)} className={`whitespace-nowrap px-3 py-1 rounded-full text-xs font-medium transition-colors ${activeCategory === cat ? 'bg-emerald-600 text-white' : 'bg-white text-gray-600 border border-gray-300 hover:bg-gray-50'}`}>
                    {cat}
                  </button>
                ))}
              </div>
            </div>

            <div className="flex-1 overflow-y-auto p-2 space-y-1 bg-gray-50/30">
              {filteredProducts.map(product => {
                const qty = cart[product.id] || 0;
                return (
                  <div key={product.id} className={`flex items-center justify-between p-2.5 rounded border transition-colors ${qty > 0 ? 'border-emerald-400 bg-emerald-50/50 shadow-sm' : 'border-transparent hover:bg-gray-100'}`}>
                    <div className="flex-1">
                      <div className="font-bold text-[15px] text-gray-800">{product.cnName}</div>
                      <div className="text-[12px] text-gray-500">{product.enName}</div>
                    </div>
                    <div className="flex items-center gap-2">
                      <span className="text-[12px] font-medium bg-gray-200 px-2 py-0.5 rounded text-gray-600 min-w-[32px] text-center">{product.unit}</span>
                      <div className="flex items-center border border-gray-300 rounded-md bg-white shadow-sm">
                        <button onClick={() => decrement(product.id)} className="px-2.5 py-1.5 text-gray-600 hover:bg-gray-100 rounded-l-md"><Minus className="w-3.5 h-3.5" /></button>
                        <input type="number" value={qty || ''} onChange={e => handleQuantityChange(product.id, e.target.value)} placeholder="0" className="w-10 text-center text-sm font-bold text-gray-700 outline-none" />
                        <button onClick={() => increment(product.id)} className="px-2.5 py-1.5 text-gray-600 hover:bg-gray-100 rounded-r-md"><Plus className="w-3.5 h-3.5" /></button>
                      </div>
                    </div>
                  </div>
                );
              })}
            </div>
          </div>
        </div>

        {/* ================= 右侧：A4 纸张预览 ================= */}
        <div className="w-full flex-1 flex justify-start lg:justify-center overflow-x-auto print-area-container pb-10">
          
          <div className="a4-paper bg-white shadow-xl relative shrink-0">
            
            {/* 纸张内部布局 (标准 A4 边距) */}
            <div className="p-[30px] sm:p-[40px] text-sm text-black font-sans flex flex-col h-full min-h-[1050px]">
              
              {/* === 新设计的正式页眉 Header === */}
              <div className="flex justify-between items-start border-b-[3px] border-slate-800 pb-5 mb-6 mt-2">
                
                {/* 左侧：公司抬头与总部地址 */}
                <div className="flex-1 pr-4">
                  <h1 className="text-3xl font-black text-slate-800 tracking-wider mb-2 leading-tight">
                    {companyName}
                  </h1>
                  <div className="text-xs text-gray-600 font-medium whitespace-pre-wrap leading-relaxed opacity-80">
                    {defaultAddress}
                  </div>
                </div>

                {/* 右侧：PO单据信息 */}
                <div className="text-right shrink-0">
                  <h2 className="text-2xl sm:text-3xl font-black text-slate-800 mb-3 tracking-widest uppercase pb-1 border-b border-gray-300 inline-block">
                    Purchase Order
                  </h2>
                  <table className="ml-auto text-sm text-right mt-2 border-collapse">
                    <tbody>
                      <tr>
                        <td className="py-1 pr-3 font-bold text-gray-500 uppercase text-xs tracking-wider">PO Number:</td>
                        <td className="py-1 font-bold text-slate-800 text-[15px]">{poNumber}</td>
                      </tr>
                      <tr>
                        <td className="py-1 pr-3 font-bold text-gray-500 uppercase text-xs tracking-wider">Order Date:</td>
                        <td className="py-1 font-bold text-slate-800 text-[15px]">{orderDate}</td>
                      </tr>
                    </tbody>
                  </table>
                </div>
              </div>

              {/* 地址栏 Addresses */}
              <div className="grid grid-cols-2 gap-8 sm:gap-12 mb-8">
                <div>
                  <h3 className="bg-slate-100 text-slate-700 font-bold px-3 py-1.5 mb-2 uppercase text-xs tracking-wider border-l-4 border-slate-400">Bill To (Invoice)</h3>
                  <div className="px-2 whitespace-pre-wrap text-gray-700 leading-relaxed font-medium text-[13px]">
                    {billTo}
                  </div>
                </div>
                <div>
                  <h3 className="bg-slate-100 text-slate-700 font-bold px-3 py-1.5 mb-2 uppercase text-xs tracking-wider border-l-4 border-slate-400">Ship To (Delivery)</h3>
                  <div className="px-2 whitespace-pre-wrap text-gray-700 leading-relaxed font-medium text-[13px]">
                    {shipTo}
                  </div>
                </div>
              </div>

              {/* 商品表格 Table */}
              <div className="flex-1 mb-8">
                <table className="w-full text-left border-collapse">
                  <thead>
                    <tr className="bg-slate-800 text-white text-[11px] sm:text-xs uppercase tracking-wider">
                      <th className="py-2.5 px-3 border border-slate-700 w-12 text-center">S/N</th>
                      <th className="py-2.5 px-3 border border-slate-700">Item Description (Eng/Malay)</th>
                      <th className="py-2.5 px-3 border border-slate-700">中文说明</th>
                      <th className="py-2.5 px-3 border border-slate-700 w-20 text-center">Qty</th>
                      <th className="py-2.5 px-3 border border-slate-700 w-16 text-center">Unit</th>
                      <th className="py-2.5 px-3 border border-slate-700 w-32 sm:w-48">Remarks</th>
                    </tr>
                  </thead>
                  <tbody>
                    {selectedItems.length === 0 ? (
                      <tr>
                        <td colSpan="6" className="py-16 text-center text-gray-400 border border-gray-300 italic">
                          No items added yet. Please select items from the left panel.
                        </td>
                      </tr>
                    ) : (
                      selectedItems.map((item, index) => (
                        <tr key={item.id} className="even:bg-gray-50 hover:bg-blue-50/30 transition-colors">
                          <td className="py-2.5 px-3 border border-gray-300 text-center text-gray-500 font-medium">{index + 1}</td>
                          <td className="py-2.5 px-3 border border-gray-300 font-bold text-slate-800">{item.enName}</td>
                          <td className="py-2.5 px-3 border border-gray-300 text-gray-600 text-xs sm:text-sm">{item.cnName}</td>
                          <td className="py-2.5 px-3 border border-gray-300 text-center font-black text-base">{item.quantity}</td>
                          <td className="py-2.5 px-3 border border-gray-300 text-center text-gray-600">{item.unit}</td>
                          <td className="py-2.5 px-3 border border-gray-300">
                            <input 
                              type="text" 
                              placeholder="Write remark..." 
                              value={remark[item.id] || ''}
                              onChange={(e) => setRemark(prev => ({ ...prev, [item.id]: e.target.value }))}
                              className="w-full bg-transparent border-b border-dotted border-gray-400 focus:border-emerald-500 outline-none text-xs pb-1 text-blue-700 font-medium placeholder:font-normal"
                            />
                          </td>
                        </tr>
                      ))
                    )}
                  </tbody>
                </table>
              </div>

              {/* 底部备注与签名 Footer */}
              <div className="mt-auto pt-6 border-t-[3px] border-slate-800 pb-4">
                <div className="grid grid-cols-2 gap-8 sm:gap-12">
                  <div>
                    <h4 className="font-bold text-slate-700 mb-2 uppercase text-[11px] tracking-wider">Special Instructions / Remarks</h4>
                    <div className="whitespace-pre-wrap text-[13px] text-gray-700 bg-gray-50 p-3 rounded border border-gray-200 min-h-[60px]">
                      {poNotes || 'None'}
                    </div>
                  </div>
                  <div className="flex flex-col items-end justify-end">
                    <div className="w-48 sm:w-64 border-b border-gray-800 pb-1 mb-2 text-center h-12">
                      {/* 预留签名区 */}
                    </div>
                    <p className="text-[10px] sm:text-xs font-bold text-gray-500 uppercase tracking-widest">Authorized Signature</p>
                  </div>
                </div>
              </div>

            </div>
          </div>
        </div>
      </main>

      {/* 打印专用样式 & 全局样式 */}
      <style dangerouslySetInnerHTML={{__html: `
        /* A4 纸张尺寸设定 (210x297mm) */
        .a4-paper {
          width: 210mm;
          min-height: 297mm;
          margin: 0 auto;
        }

        /* 隐藏滚动条 */
        .hide-scrollbar::-webkit-scrollbar { display: none; }
        .hide-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
        
        /* 隐藏数字输入框箭头 */
        input[type=number]::-webkit-inner-spin-button, 
        input[type=number]::-webkit-outer-spin-button { -webkit-appearance: none; margin: 0; }

        /* ========= 打印核心设置 ========= */
        @media print {
          @page {
            size: A4 portrait;
            margin: 0;
          }
          
          body {
            background: white !important;
            margin: 0 !important;
            padding: 0 !important;
          }

          /* 隐藏左侧面板和导航栏 */
          .hide-on-print {
            display: none !important;
          }

          /* 打印区域铺满页面 */
          .print-area-container {
            width: 100% !important;
            margin: 0 !important;
            padding: 0 !important;
            overflow: visible !important;
            justify-content: flex-start !important;
          }

          .a4-paper {
            width: 100% !important;
            box-shadow: none !important;
            margin: 0 !important;
            border: none !important;
            min-height: auto !important;
          }

          /* 表格打印防断页优化 */
          table { page-break-inside: auto; }
          tr { page-break-inside: avoid; page-break-after: auto; }
          thead { display: table-header-group; }
          
          /* 强制保留所有背景颜色和边框 */
          * {
            -webkit-print-color-adjust: exact !important;
            print-color-adjust: exact !important;
          }
        }
      `}} />
    </div>
  );
}


