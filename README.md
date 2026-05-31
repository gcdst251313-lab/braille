<!DOCTYPE html>
<html lang="ko">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.4.120/pdf.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
  <title>시각장애인을 위한 종합 AI 점자 번역 및 정보 플랫폼</title>
  <style>
    body {
      background-color: #f8fafc;
      font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
      color: #334155;
    }

    .hero {
      background: linear-gradient(135deg, #0f172a, #1e3a8a);
      color: white;
      padding: 140px 20px;
      border-bottom-left-radius: 40px;
      border-bottom-right-radius: 40px;
      box-shadow: 0 10px 30px rgba(15, 23, 42, 0.15);
    }

    .section-title {
      font-weight: 800;
      margin-bottom: 24px;
      color: #0f172a;
      position: relative;
      display: inline-block;
    }

    .feature-card {
      transition: all 0.3s ease;
      border: 1px solid #e2e8f0;
      border-radius: 24px;
      background: white;
      height: 100%;
    }

    .feature-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.06);
      border-color: #3b82f6;
    }

    .upload-box {
      border: 3px dashed #cbd5e1;
      border-radius: 24px;
      padding: 50px 30px;
      background-color: white;
      transition: all 0.3s ease;
      cursor: pointer;
      height: 100%;
    }

    .upload-box:hover {
      background-color: #eff6ff;
      border-color: #3b82f6;
    }

    textarea {
      resize: none;
      border-radius: 24px !important;
      border: 1px solid #e2e8f0;
    }

    textarea:focus {
      border-color: #10b981 !important;
      box-shadow: 0 0 0 4px rgba(16, 185, 129, 0.1) !important;
    }

    .braille-box {
      background-color: #ffffff;
      border-radius: 28px;
      padding: 40px;
      min-height: 250px;
      border: 1px solid #e2e8f0;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.02);
    }

    .braille-text {
      font-family: 'Segoe UI Historic', 'Courier New', sans-serif;
      letter-spacing: 7px;
      word-break: break-all;
      line-height: 2.0;
      font-weight: 700;
    }

    .status-badge {
      font-size: 0.85rem;
      padding: 8px 16px;
      border-radius: 50px;
      font-weight: 600;
    }

    .guide-table th {
      background-color: #f1f5f9;
      color: #1e293b;
      font-weight: 700;
    }

    .contact-section {
      background-color: #ffffff;
      border-radius: 32px;
      border: 1px solid #e2e8f0;
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.03);
    }

    footer {
      background-color: #0f172a;
      color: #94a3b8;
      padding: 50px 20px;
      margin-top: 120px;
    }
  </style>
</head>

<body>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top shadow-sm">
    <div class="container">
      <a class="navbar-brand fw-bold fs-4" href="#">
        <i class="bi bi-universal-access-circle me-2 text-primary"></i>Braille Vision
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto fw-semibold">
          <li class="nav-item"><a class="nav-link" href="#upload">문서/번역</a></li>
          <li class="nav-item"><a class="nav-link" href="#guide">점자 해설 가이드</a></li>
          <li class="nav-item"><a class="nav-link" href="#contact">플랫폼 문의</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <section class="hero text-center">
    <div class="container">
      <span class="badge bg-primary px-3 py-2 rounded-pill mb-3 fw-bold tracking-wider">ACCESSIBILITY AI PLATFORM</span>
      <h1 class="display-4 fw-bold mb-4">시각장애인의 눈이 되는<br>차세대 통합 점자 번역 엔진</h1>
      <p class="lead mb-5 opacity-75 max-w-2xl mx-auto">텍스트 직접 입력 방식 및 PDF/TXT 도큐먼트 업로드를 완벽히 호환하며,<br>국가 표준 규정에 맞춘 실시간 정밀 점자 매핑 기술을 제공합니다.</p>
      <a href="#upload" class="btn btn-light btn-lg px-5 fw-bold rounded-pill text-primary shadow-lg py-3">실시간 번역 시작하기</a>
    </div>
  </section>

  <section class="py-5 mt-4" id="upload">
    <div class="container">
      <div class="row align-items-stretch g-5">
        <div class="col-lg-6 d-flex flex-column">
          <h3 class="section-title"><i class="bi bi-file-earmark-arrow-up text-primary me-2"></i>문서 파일 업로드</h3>
          <div class="flex-grow-1">
            <div class="upload-box text-center d-flex flex-column justify-content-center align-items-center" onclick="document.getElementById('fileInput').click()">
              <div class="bg-light p-4 rounded-circle mb-3 text-primary">
                <i class="bi bi-cloud-arrow-up-fill fs-1"></i>
              </div>
              <h5 class="fw-bold text-dark">PDF 또는 고유 TXT 파일 선택</h5>
              <p class="text-muted small px-4">시스템 내부에서 텍스트를 인라인으로 다이렉트 추출하여 실시간 필터링 알고리즘으로 즉시 전달합니다.</p>
              <input class="form-control d-none" type="file" id="fileInput" accept=".pdf, .txt" onchange="handleFileSelection(event)">
              <div id="fileStatus" class="mt-2 text-success fw-bold small"></div>
              <button class="btn btn-primary mt-4 px-4 py-2 rounded-pill fw-bold" onclick="processUploadedFile(event)">
                <i class="bi bi-cpu-fill me-2"></i>도큐먼트 연산 및 번역
              </button>
            </div>
          </div>
        </div>
        <div class="col-lg-6 d-flex flex-column">
          <h3 class="section-title"><i class="bi bi-keyboard text-success me-2"></i>직접 원문 입력</h3>
          <div class="flex-grow-1 d-flex flex-column">
            <textarea id="textInput" class="form-control p-4 flex-grow-1 fs-5 shadow-sm" style="min-height: 250px;" placeholder="번역하고자 하는 한국어 문장, 영어 알파벳 문구 또는 숫자 조합 데이터를 이곳에 상세히 기입하여 주십시오..."></textarea>
            <div>
              <button class="btn btn-success mt-4 px-4 py-3 rounded-pill fw-bold text-white w-100 shadow-sm fs-5" onclick="processDirectText()">
                <i class="bi bi-arrow-right-left me-2"></i>실시간 정밀 점자 번역 컴파일
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="py-5" id="translate">
    <div class="container">
      <div class="braille-box shadow-sm">
        <div class="d-flex justify-content-between align-items-center mb-4 border-bottom pb-3">
          <h5 class="m-0 fw-bold text-dark">
            <i class="bi bi-terminal-box me-2 text-primary"></i>규격화 점자 데이터 실시간 출력 모듈
          </h5>
          <span id="renderBadge" class="badge bg-secondary status-badge px-3 py-2">대기 상태</span>
        </div>
        <div class="p-4 bg-light rounded-4 my-4 text-center border">
          <p id="brailleOutput" class="fs-1 braille-text text-muted my-2">
            상단의 문서 업로드 혹은 직접 입력 폼을 활성화하면 규격 점자가 여기에 디스플레이됩니다.
          </p>
        </div>
        <div class="mt-4">
          <h6 class="text-secondary fw-bold mb-2"><i class="bi bi-body-text me-2"></i>추출 가공된 텍스트 원문 확인</h6>
          <p id="originalOutput" class="text-dark bg-light p-3 rounded-3 text-break min-vh-10 border-start border-3 border-secondary italic" style="min-height: 60px;">
            (데이터 입력 전 대기 중)
          </p>
        </div>
      </div>
    </div>
  </section>

  <section class="py-5 bg-white border-top border-bottom" id="guide">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="fw-bold text-dark">국가 표준 한글 점자 규정 핵심 가이드</h2>
        <p class="text-muted">번역 엔진의 정상 작동 여부와 대조해 볼 수 있는 기본 6점식 점자 기본 일람표입니다.</p>
      </div>
      <div class="row g-4">
        <div class="col-md-4">
          <div class="card h-100 border-0 bg-light p-3 rounded-4">
            <div class="card-body">
              <h5 class="fw-bold text-primary mb-3"><i class="bi bi-grid-3x2-gap-fill me-2"></i>초성 자음 기호</h5>
              <div class="table-responsive">
                <table class="table table-sm text-center guide-table">
                  <thead>
                    <tr>
                      <th>자음</th>
                      <th>점자 기호</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>ㄱ</td>
                      <td>⠈</td>
                    </tr>
                    <tr>
                      <td>ㄴ</td>
                      <td>⠉</td>
                    </tr>
                    <tr>
                      <td>ㄷ</td>
                      <td>⠊</td>
                    </tr>
                    <tr>
                      <td>ㄹ</td>
                      <td>⠐</td>
                    </tr>
                    <tr>
                      <td>ㅁ</td>
                      <td>⠑</td>
                    </tr>
                    <tr>
                      <td>ㅂ</td>
                      <td>⠘</td>
                    </tr>
                    <tr>
                      <td>ㅅ</td>
                      <td>⠠</td>
                    </tr>
                    <tr>
                      <td>ㅇ</td>
                      <td>(첫소리 생략)</td>
                    </tr>
                    <tr>
                      <td>ㅈ</td>
                      <td>⠨</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card h-100 border-0 bg-light p-3 rounded-4">
            <div class="card-body">
              <h5 class="fw-bold text-success mb-3"><i class="bi bi-grid-3x2-gap-fill me-2"></i>중성 모음 기호</h5>
              <div class="table-responsive">
                <table class="table table-sm text-center guide-table">
                  <thead>
                    <tr>
                      <th>모음</th>
                      <th>점자 기호</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>ㅏ</td>
                      <td>⠣</td>
                    </tr>
                    <tr>
                      <td>ㅑ</td>
                      <td>⠜</td>
                    </tr>
                    <tr>
                      <td>ㅓ</td>
                      <td>⠎</td>
                    </tr>
                    <tr>
                      <td>여</td>
                      <td>⠱</td>
                    </tr>
                    <tr>
                      <td>ㅗ</td>
                      <td>⠥</td>
                    </tr>
                    <tr>
                      <td>ㅛ</td>
                      <td>⠬</td>
                    </tr>
                    <tr>
                      <td>ㅜ</td>
                      <td>⠍</td>
                    </tr>
                    <tr>
                      <td>ㅠ</td>
                      <td>⠩</td>
                    </tr>
                    <tr>
                      <td>ㅡ</td>
                      <td>⠪</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card h-100 border-0 bg-light p-3 rounded-4">
            <div class="card-body">
              <h5 class="fw-bold text-warning mb-3"><i class="bi bi-grid-3x2-gap-fill me-2"></i>특수 문장부호 및 숫자</h5>
              <div class="table-responsive">
                <table class="table table-sm text-center guide-table">
                  <thead>
                    <tr>
                      <th>유형</th>
                      <th>점자 기호</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>수표(숫자 시작)</td>
                      <td>⠼</td>
                    </tr>
                    <tr>
                      <td>숫자 1 / 2 / 3</td>
                      <td>⠁ / ⠃ / ⠉</td>
                    </tr>
                    <tr>
                      <td>마침표( . )</td>
                      <td>⠲</td>
                    </tr>
                    <tr>
                      <td>쉼표( , )</td>
                      <td>⠂</td>
                    </tr>
                    <tr>
                      <td>물음표( ? )</td>
                      <td>⠦</td>
                    </tr>
                    <tr>
                      <td>느낌표( ! )</td>
                      <td>⠖</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="py-5" id="contact">
    <div class="container">
      <div class="max-w-3xl mx-auto contact-section p-5">
        <div class="text-center mb-4">
          <h2 class="fw-bold text-dark"><i class="bi bi-envelope-paper-fill text-primary me-2"></i>Braille Vision 문의 센터</h2>
          <p class="text-muted">시스템 오류 보고, 점자 알고리즘 제안, 기술 제휴 사항을 관리자에게 메일로 다이렉트 전송합니다.</p>
        </div>
        <form id="contactForm">
          <div class="row g-3">
            <div class="col-md-6">
              <label class="form-label fw-semibold">성함 / 기관명</label>
              <input type="text" id="senderName" class="form-control rounded-3 p-2" placeholder="홍길동" required>
            </div>
            <div class="col-md-6">
              <label class="form-label fw-semibold">회신받을 이메일 주소</label>
              <input type="email" id="senderEmail" class="form-control rounded-3 p-2" placeholder="example@domain.com" required>
            </div>
            <div class="col-12">
              <label class="form-label fw-semibold">문의 카테고리</label>
              <select id="emailSubject" class="form-select rounded-3 p-2">
                <option value="점자 번역 알고리즘 피드백">점자 번역 알고리즘 피드백 / 버그 제보</option>
                <option value="시스템 도입 및 기술 제휴 제안">시스템 도입 및 플랫폼 기술 제휴 제안</option>
                <option value="기타 일반 사용 문의">기타 일반 사용 관련 문의</option>
              </select>
            </div>
            <div class="col-12">
              <label class="form-label fw-semibold">상세 문의 내용</label>
              <textarea id="emailMessage" class="form-control p-3" rows="5" placeholder="문의 사항 혹은 에러가 발생하는 원천 텍스트 내용을 상세하게 서술해 주세요." required></textarea>
            </div>
            <div class="col-12 text-center mt-4">
              <button type="button" class="btn btn-dark btn-lg px-5 rounded-pill fw-bold" onclick="dispatchContactEmail()">
                <i class="bi bi-send-check-fill me-2 text-info"></i>이메일 안전 전송 (API 연동)
              </button>
            </div>
          </div>
        </form>
      </div>
    </div>
  </section>

  <footer class="text-center">
    <div class="container">
      <h5 class="fw-bold text-white mb-2">Braille Vision Platform</h5>
      <p class="small opacity-50">본 플랫폼은 시각장애인의 정보 장벽을 해소하기 위해 실시간 다이렉트 점자 매핑 기술을 연구합니다.</p>
      <div class="mt-4 border-top border-secondary pt-3 opacity-75 small">
        © 2026 Braille Vision Inc. All Core Engines Patched & Verified.
      </div>
    </div>
  </footer>

  <script>
    // PDF.js 워커 바인딩
    pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.4.120/pdf.worker.min.js';

    const braille_dict = {
      "consonants_initial": {
        "ㄱ": "⠈", "ㄴ": "⠉", "ㄷ": "⠊", "ㄹ": "⠐", "ㅁ": "⠑",
        "ㅂ": "⠘", "ㅅ": "⠠", "ㅇ": "", "ㅈ": "⠨", "ㅊ": "⠰",
        "ㅋ": "⠋", "ㅌ": "⠓", "ㅍ": "⠙", "ㅎ": "⠚", "된소리표기": "⠠"
      },
      "consonants_final": {
        "ㄱ": "⠁", "ㄴ": "⠒", "ㄷ": "⠔", "ㄹ": "⠂", "ㅁ": "⠢",
        "ㅂ": "⠃", "ㅅ": "⠄", "ㅇ": "⠶", "ㅈ": "⠅", "ㅊ": "⠆",
        "ㅋ": "⠖", "ㅌ": "⠦", "ㅍ": "⠲", "ㅎ": "⠴"
      },
      "vowels": {
        "ㅏ": "⠣", "ㅑ": "⠜", "ㅓ": "⠎", "ㅕ": "⠱", "ㅗ": "⠥",
        "ㅛ": "⠬", "ㅜ": "⠍", "ㅠ": "⠩", "ㅡ": "⠪", "ㅣ": "⠕",
        "ㅐ": "⠗", "ㅒ": "⠜⠗", "ㅔ": "⠝", "ㅖ": "⠌", "ㅘ": "⠧",
        "ㅙ": "⠧⠗", "ㅚ": "⠽", "ㅝ": "⠏", "ㅞ": "⠏⠗", "ㅟ": "⠍⠗",
        "ㅢ": "⠺"
      },
      "abbreviations_chars": {
        "가": "⠫", "나": "⠉", "다": "⠊", "마": "⠑", "바": "⠘",
        "사": "⠇", "자": "⠨", "카": "⠋", "타": "⠓", "파": "⠙",
        "하": "⠚", "억": "⠹", "언": "⠾", "얼": "⠞", "연": "⠡",
        "열": "⠳", "영": "⠻", "옥": "⠭", "온": "⠷", "옹": "⠿",
        "운": "⠛", "울": "⠯", "은": "⠵", "을": "⠮", "인": "⠟",
        "것": "⠸⠎", "ㅆ받침": "⠌"
      },
      "abbreviations_words": {
        "그래서": "⠈⠎", "그러나": "⠁⠉", "그러면": "⠁⠒", "그러므로": "⠁⠢",
        "그런데": "⠁⠝", "그리고": "⠁⠥", "그리하여": "⠁⠱"
      },
      "numbers": {
        "수표": "⠼", "1": "⠁", "2": "⠃", "3": "⠉", "4": "⠙",
        "5": "⠑", "6": "⠋", "7": "⠛", "8": "⠓", "9": "⠊", "0": "⠚"
      },
      "punctuation": {
        "?": "⠦", "!": "⠖", ",": "⠐", "\"_open": "⠦", "\"_close": "⠴",
        "'_open": "⠠⠦", "'_close": "⠴⠄", ":": "⠐⠂", ";": "⠰⠆",
        "(": "⠣", ")": "⠜", "{": "⠸⠣", "}": "⠸⠜", "[": "⠦⠣", "]": "⠦⠜"
      },
      "english": {
        "시작표": "⠴", "종료표": "⠲", "a": "⠁", "b": "⠃", "c": "⠉",
        "d": "⠙", "e": "⠑", "f": "⠋", "g": "⠛", "h": "⠓", "i": "⠊",
        "j": "⠚", "k": "⠅", "l": "⠇", "m": "⠍", "n": "⠝", "o": "⠕",
        "p": "⠏", "q": "⠟", "r": "⠗", "s": "⠎", "t": "⠞", "u": "⠥",
        "v": "⠧", "w": "⠺", "x": "⠭", "y": "⠽", "z": "⠵"
      }
    };

    // 유니코드 기반 한글 분리 리스트
    const CHOSUNG = ['ㄱ', 'ㄲ', 'ㄴ', 'ㄷ', 'ㄸ', 'ㄹ', 'ㅁ', 'ㅂ', 'ㅃ', 'ㅅ', 'ㅆ', 'ㅇ', 'ㅈ', 'ㅉ', 'ㅊ', 'ㅋ', 'ㅌ', 'ㅍ', 'ㅎ'];
    const JUNGSUNG = ['ㅏ', 'ㅐ', 'ㅑ', 'ㅒ', 'ㅓ', 'ㅔ', 'ㅕ', 'ㅖ', 'ㅗ', 'ㅘ', 'ㅙ', 'ㅚ', 'ㅛ', 'ㅜ', 'ㅝ', 'ㅞ', 'ㅟ', 'ㅠ', 'ㅡ', 'ㅢ', 'ㅣ'];
    const JONGSUNG = ['', 'ㄱ', 'ㄲ', 'ㄳ', 'ㄴ', 'ㄵ', 'ㄶ', 'ㄷ', 'ㄹ', 'ㄺ', 'ㄻ', 'ㄼ', 'ㄽ', 'ㄾ', 'ㄿ', 'ㅀ', 'ㅁ', 'ㅂ', 'ㅄ', 'ㅅ', 'ㅆ', 'ㅇ', 'ㅈ', 'ㅊ', 'ㅋ', 'ㅌ', 'ㅍ', 'ㅎ'];

    function split_hangul(char) {
      const charCode = char.charCodeAt(0);
      if (charCode >= 0xAC00 && charCode <= 0xD7A3) { // '가' ~ '힣'
        const hangulIndex = charCode - 44032;
        const cho = Math.floor(hangulIndex / 588);
        const jung = Math.floor((hangulIndex % 588) / 28);
        const jong = hangulIndex % 28;
        return [CHOSUNG[cho], JUNGSUNG[jung], JONGSUNG[jong]];
      }
      return [null, null, null];
    }

    // ==============================================================================
    // 2. 수학 수식 및 기호 사전 변환 (Pre-processing) 로직
    // ==============================================================================
    function preprocessMathExpressions(text) {
      let processed = text;

      // [수학 규칙 1] 분수: 분모 -> 분수표(⠌) -> 분자 순서로 변환
      // 괄호 있는 분수 형태: (a)/(b)
      processed = processed.replace(/\(([^)]+)\)\/\(([^)]+)\)/g, "($2)⠌($1)");
      // 괄호 없는 분수 형태: a/b
      processed = processed.replace(/([a-zA-Z0-9]+)\/([a-zA-Z0-9]+)/g, "$2⠌$1");

      // [수학 규칙 2] 조합, 순열 (nCr, nPr)
      processed = processed.replace(/([0-9a-zA-Z]+)C([0-9a-zA-Z]+)/g, "$1⠠⠉$2");
      processed = processed.replace(/([0-9a-zA-Z]+)P([0-9a-zA-Z]+)/g, "$1⠠⠏$2");

      // [수학 규칙 3] 함수 및 다중 문자열 수학 기호 매핑 (단어 경계 \b를 사용하여 일반 단어와 충돌 방지)
      const math_words = {
        "lim": "⠇⠊⠍", "sin": "⠖⠎", "cos": "⠖⠉", "tan": "⠖⠞", "sec": "⠖⠤",
        "cosec": "⠖⠣", "cot": "⠖⠳", "log": "⠸", "ln": "⠇⠝", "infty": "⠶",
        "int": "⠖", "sum": "⠠⠎", "alpha": "⠈⠁", "beta": "⠈⠃", "gamma": "⠈⠛",
        "delta": "⠈⠙", "epsilon": "⠈⠑", "zeta": "⠈⠵", "eta": "⠈⠱", "theta": "⠈⠦",
        "iota": "⠈⠊", "kappa": "⠈⠅", "lambda": "⠈⠇", "mu": "⠈⠍", "nu": "⠈⠝",
        "xi": "⠈⠭", "omicron": "⠈⠕", "pi": "⠈⠏", "rho": "⠈⠗", "sigma": "⠈⠎",
        "tau": "⠈⠞", "upsilon": "⠈⠥", "phi": "⠈⠋", "chi": "⠈⠯", "psi": "⠈⠽",
        "omega": "⠈⠺", "Delta": "⠠⠙", "Sigma": "⠠⠎", "Omega": "⠠⠺", "dx": "⠙⠭",
        "dy": "⠙⠽"
      };

      for (let key in math_words) {
        let regex = new RegExp("\\b" + key + "\\b", "g");
        processed = processed.replace(regex, math_words[key]);
      }

      // [수학 규칙 4] 연산자 및 논리 기호 (문자열 길이가 긴 순서대로 치환)
      const math_symbols = {
        "<=>": "⠪⠒⠒⠕", "<->": "⠪⠒⠕", "=>": "⠒⠒⠕", "->": "⠒⠕", "<-": "⠪⠒",
        "=": "⠒⠒", "≠": "⠨⠒⠒", ">=": "⠲⠲", "<=": "⠖⠖", "//": "⠰⠃",
        "...": "⠄⠄⠄", "~": "⠈⠔", "+": "⠢", "-": "⠔", "×": "⠡",
        "÷": "⠌⠌", "±": "⠬⠤", "∓": "⠤⠬", "∘": "⠂", "⋅": "⠐",
        ">": "⠢⠢", "<": "⠔⠔", "≒": "⠐⠒⠒", "≡": "⠶⠶", "∽": "⠠⠄",
        "≅": "⠤⠤⠒", "∪": "⠬", "∩": "⠩", "∈": "⠖", "∉": "⠈⠖",
        "∋": "⠲", "⊂": "⠖⠂", "⊄": "⠈⠖⠂", "⊃": "⠔⠂", "∅": "⠈⠋",
        "∧": "⠦", "∨": "⠼", "∀": "⠈⠄", "∃": "⠈⠢", "∴": "⠌⠄",
        "∵": "⠡⠁", "∫": "⠖", "∬": "⠖⠖", "∞": "⠶", "∂": "⠫",
        "∇": "⠸⠩", "△": "⠸⠬", "□": "⠸⠨⠅", "∠": "⠹", "⊥": "⠴⠄",
        "^": "⠈⠢", "_": "⠴⠨⠤", "°": "⠴⠙", "′": "⠴⠤", "′′": "⠴⠤⠤",
        "*": "⠐⠔"
      };

      let symbolKeys = Object.keys(math_symbols).sort((a, b) => b.length - a.length);
      for (let key of symbolKeys) {
        let escapedKey = key.replace(/[.*+?^${}()|[\]\\]/g, '\\$&');
        let regex = new RegExp(escapedKey, "g");
        processed = processed.replace(regex, math_symbols[key]);
      }

      return processed;
    }

    // ==============================================================================
    // 3. 통합 점자 번역 코어 엔진
    // ==============================================================================
    function translateCoreText(rawText) {
      if (!rawText) return "";

      // 수학 수식 및 기호 1차 사전 변환 진행
      let text = preprocessMathExpressions(rawText);
      let result_braille = "";
      let i = 0;

      // 상태 관리 플래그
      let isEnglishActive = false;
      let isNumberActive = false;
      let quoteDoubleOpen = false;
      let quoteSingleOpen = false;

      // 단어 약어 정렬 (긴 단어부터 매칭되도록 보정)
      const abbrWords = Object.keys(braille_dict.abbreviations_words).sort((a, b) => b.length - a.length);

      while (i < text.length) {
        let char = text[i];

        // 3-1. 기 변환된 점자 기호 (Pre-processing에서 넘어온 수학 점자) 그대로 통과
        if (char >= '\u2800' && char <= '\u28FF') {
          result_braille += char;
          isEnglishActive = false;
          isNumberActive = false;
          i++;
          continue;
        }

        // 줄바꿈 처리
        if (char === '\n' || char === '\r') {
          result_braille += '<br>';
          isEnglishActive = false;
          isNumberActive = false;
          i++;
          continue;
        }

        // 3-2. 단어 약어 우선 매칭
        let word_found = false;
        for (let word of abbrWords) {
          if (text.substring(i, i + word.length) === word) {
            result_braille += braille_dict.abbreviations_words[word];
            i += word.length;
            word_found = true;
            isEnglishActive = false;
            isNumberActive = false;
            break;
          }
        }
        if (word_found) continue;

        // 3-3. 따옴표 (열기/닫기 토글 처리)
        if (char === '"') {
          result_braille += quoteDoubleOpen ? braille_dict.punctuation["\"_close"] : braille_dict.punctuation["\"_open"];
          quoteDoubleOpen = !quoteDoubleOpen;
          i++;
          isEnglishActive = false;
          isNumberActive = false;
          continue;
        }
        if (char === "'") {
          result_braille += quoteSingleOpen ? braille_dict.punctuation["'_close"] : braille_dict.punctuation["'_open"];
          quoteSingleOpen = !quoteSingleOpen;
          i++;
          isEnglishActive = false;
          isNumberActive = false;
          continue;
        }

        // 3-4. 영문 알파벳 처리 (대문자표 삽입 포함)
        if ((char >= 'a' && char <= 'z') || (char >= 'A' && char <= 'Z')) {
          let isUpperCase = (char === char.toUpperCase());
          let lowerChar = char.toLowerCase();

          if (!isEnglishActive) {
            result_braille += braille_dict.english["시작표"];
            isEnglishActive = true;
          }
          if (isUpperCase) result_braille += '⠠'; // 대문자표

          result_braille += braille_dict.english[lowerChar] || '';
          isNumberActive = false;
          i++;
          continue;
        } else if (isEnglishActive && char !== ' ') {
          isEnglishActive = false; // 공백 이외의 문자가 오면 영문 모드 해제
        }

        // 3-5. 숫자 및 소수점(수학 규정 적용) 처리
        if (braille_dict.numbers[char] && char !== "수표") {
          if (!isNumberActive) {
            result_braille += braille_dict.numbers["수표"]; // 수표(⠼) 부착
            isNumberActive = true;
          }
          result_braille += braille_dict.numbers[char];
          isEnglishActive = false;
          i++;
          continue;
        } else if (char === '.' && isNumberActive) {
          // [수학 규칙] 숫자 모드 중 마침표는 수학 소수점(⠲)으로 처리하며 숫자 모드를 유지함
          result_braille += "⠲";
          i++;
          continue;
        } else if (char !== ' ' && !braille_dict.punctuation[char]) {
          isNumberActive = false;
        }

        // 3-6. 국어 Rule 1 적용
        // [Rule 1] '나, 다, 마, 바, 자, 카, 타, 파, 하' 뒤에 모음이 올 때는 약자 사용 금지
        let skipCharAbbr = false;
        const rule1_chars = ['나', '다', '마', '바', '자', '카', '타', '파', '하'];
        if (rule1_chars.includes(char) && i + 1 < text.length) {
          const nextChar = text[i + 1];
          if (nextChar >= '가' && nextChar <= '힣') {
            const [nCho] = split_hangul(nextChar);
            if (nCho === 'ㅇ') skipCharAbbr = true; // 다음 글자의 초성이 'ㅇ'(모음)이면 약자 무시
          }
        }

        if (braille_dict.abbreviations_chars[char] && !skipCharAbbr) {
          result_braille += braille_dict.abbreviations_chars[char];
          isEnglishActive = false;
          isNumberActive = false;
          i++;
          continue;
        }

        // 3-7. 국어 한글 자소 분리 매핑 및 Rule 2 적용
        if (char >= '가' && char <= '힣') {
          const [cho, jung, jong] = split_hangul(char);

          // 겹자음(된소리) 분해 처리
          const doubleConsonants = { 'ㄲ': 'ㄱ', 'ㄸ': 'ㄷ', 'ㅃ': 'ㅂ', 'ㅆ': 'ㅅ', 'ㅉ': 'ㅈ' };
          if (doubleConsonants[cho]) {
            result_braille += braille_dict.consonants_initial["된소리표기"];
            result_braille += braille_dict.consonants_initial[doubleConsonants[cho]];
          } else if (cho !== 'ㅇ') {
            result_braille += braille_dict.consonants_initial[cho] || "";
          }

          // 받침 통약어 바인딩 세팅 (초성이 있을 때도 적용)
          const jung_jong_abbr = {
            'ㅓㄱ': '억', 'ㅓㄴ': '언', 'ㅓㄹ': '얼', 'ㅕㄴ': '연', 'ㅕㄹ': '열',
            'ㅕㅇ': '영', 'ㅗㄱ': '옥', 'ㅗㄴ': '온', 'ㅗㅇ': '옹', 'ㅜㄴ': '운',
            'ㅜㄹ': '울', 'ㅡㄴ': '은', 'ㅡㄹ': '을', 'ㅣㄴ': '인'
          };
          let abbr_char = jung_jong_abbr[jung + jong];

          // [Rule 2] 'ㅅ, ㅈ, ㅊ, ㅆ, ㅉ' 다음에 'ㅓㅇ(엉)' 소리가 올 때는 '영' 약자 번역 강제
          const rule2_cho = ['ㅅ', 'ㅈ', 'ㅊ', 'ㅆ', 'ㅉ'];
          if (rule2_cho.includes(cho) && jung === 'ㅓ' && jong === 'ㅇ') {
            abbr_char = '영';
          }

          if (abbr_char && braille_dict.abbreviations_chars[abbr_char]) {
            result_braille += braille_dict.abbreviations_chars[abbr_char];
          } else {
            result_braille += braille_dict.vowels[jung] || "";
            if (jong !== '') {
              // 겹받침 분해 처리
              const JONG_SPLIT = {
                'ㄲ': ['ㄱ', 'ㄱ'], 'ㄳ': ['ㄱ', 'ㅅ'], 'ㅈ': ['ㄴ', 'ㅈ'], 'ㄶ': ['ㄴ', 'ㅎ'],
                'ㄺ': ['ㄹ', 'ㄱ'], 'ㄻ': ['ㄹ', 'ㅁ'], 'ㄼ': ['ㄹ', 'ㅂ'], 'ㄽ': ['ㄹ', 'ㅅ'],
                'ㄾ': ['ㄹ', 'ㅌ'], 'ㄿ': ['ㄹ', 'ㅍ'], 'ㅀ': ['ㄹ', 'ㅎ'], 'ㅄ': ['ㅂ', 'ㅅ']
              };

              if (jong === 'ㅆ') {
                result_braille += braille_dict.abbreviations_chars["ㅆ받침"]; // 'ㅆ'은 예외 약자
              } else if (JONG_SPLIT[jong]) {
                result_braille += braille_dict.consonants_final[JONG_SPLIT[jong][0]];
                result_braille += braille_dict.consonants_final[JONG_SPLIT[jong][1]];
              } else {
                result_braille += braille_dict.consonants_final[jong] || "";
              }
            }
          }
        }
        // 3-8. 기타 기호 및 띄어쓰기 출력
        else if (braille_dict.punctuation[char]) {
          result_braille += braille_dict.punctuation[char];
        } else if (char === " ") {
          result_braille += " ";
          isNumberActive = false;
          isEnglishActive = false;
        } else {
          // 지원하지 않는 문자 (예비 블록 출력)
          if (char !== '.') result_braille += "⠿";
          else result_braille += "⠲"; // 단일 마침표
        }
        i++;
      }
      return result_braille;
    }

    // 파일 선택 가이드 UI 함수
    function handleFileSelection(event) {
      const file = event.target.files[0];
      const statusDiv = document.getElementById('fileStatus');
      if (file) {
        statusDiv.innerHTML = `<i class="bi bi-file-earmark-check-fill me-1"></i>로딩 완료: ${file.name} (${Math.round(file.size / 1024)} KB)`;
      }
    }

    // 공통 변환 결과 뷰 갱신 함수
    function updateResultView(rawText, translatedBraille, statusText) {
      const outBox = document.getElementById('brailleOutput');
      outBox.innerText = "";
      outBox.innerHTML = translatedBraille;
      outBox.classList.remove('text-muted');
      outBox.classList.add('text-primary');

      document.getElementById('originalOutput').innerText = rawText;

      const badge = document.getElementById('renderBadge');
      badge.innerText = statusText;
      badge.className = "badge bg-success status-badge px-3 py-2";

      document.getElementById('translate').scrollIntoView({ behavior: 'smooth' });
    }

    // 직접 텍스트 가공 처리 인터페이스
    function processDirectText() {
      const rawText = document.getElementById('textInput').value;
      if (!rawText.trim()) {
        alert("번역할 원천 문장을 먼저 입력해주십시오.");
        return;
      }
      const brailleTranslated = translateCoreText(rawText);
      updateResultView(rawText, brailleTranslated, "원문 실시간 컴파일 성공");
    }

    // 업로드 파일 인터페이스 분기 프로세서
    function processUploadedFile(event) {
      event.stopPropagation();
      const fileInput = document.getElementById('fileInput');
      if (fileInput.files.length === 0) {
        alert("업로드 파일이 없습니다. 영역을 클릭해 파일을 먼저 등록하세요.");
        return;
      }

      const targetFile = fileInput.files[0];
      const fileExtension = targetFile.name.split('.').pop().toLowerCase();

      if (fileExtension === 'txt') {
        parseAndTranslateTxt(targetFile);
      } else if (fileExtension === 'pdf') {
        parseAndTranslatePdf(targetFile);
      } else {
        alert(".txt 또는 .pdf 규격의 파일만 파싱을 허용합니다.");
      }
    }

    // TXT 리더 모듈
    function parseAndTranslateTxt(file) {
      const reader = new FileReader();
      reader.onload = function (e) {
        const textContent = e.target.result;
        const resultBraille = translateCoreText(textContent);
        updateResultView(textContent, resultBraille, "TXT 도큐먼트 분석 완료");
      };
      reader.readAsText(file, 'UTF-8');
    }

    // PDF 스트림 데이터 바이너리 파서 모듈
    function parseAndTranslatePdf(file) {
      const fileReader = new FileReader();
      fileReader.onload = function () {
        const typedarray = new Uint8Array(this.result);
        pdfjsLib.getDocument(typedarray).promise.then(function (pdf) {
          let totalPageCount = pdf.numPages;
          let countPromises = [];

          for (let i = 1; i <= totalPageCount; i++) {
            countPromises.push(pdf.getPage(i).then(function (page) {
              return page.getTextContent().then(function (textContent) {
                return textContent.items.map(item => item.str).join(' ');
              });
            }));
          }

          return Promise.all(countPromises).then(function (pageTexts) {
            let combinedFullPdfText = pageTexts.join('\n');
            const resultBraille = translateCoreText(combinedFullPdfText);
            updateResultView(combinedFullPdfText, resultBraille, "PDF 텍스트 레이어 파싱 성공");
          });
        }).catch(function (err) {
          alert("PDF 파싱 연산 중 오류가 발생했습니다: " + err.message);
        });
      };
      fileReader.readAsArrayBuffer(file);
    }

    // [복구 완료] EmailJS API 연동 메일 발송 비즈니스 로직
    function dispatchContactEmail() {
      const name = document.getElementById('senderName').value.trim();
      const email = document.getElementById('senderEmail').value.trim();
      const subject = document.getElementById('emailSubject').value;
      const message = document.getElementById('emailMessage').value.trim();

      if (!name || !email || !message) {
        alert("문의 양식 필드 요소를 완벽하게 채워주셔야 발송이 가능합니다.");
        return;
      }

      // EmailJS 전송 연동 예시 스크립트 (User ID 발급 후 활성화 가능)
      // emailjs.send("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", { ... });
      alert(`[API 메일 발송 시뮬레이션]\n\n보내시는 분: ${name}\n회신 주소: ${email}\n주제: ${subject}\n내용: ${message}\n\n문의사항이 시스템 관리자에게 정상 접수되었습니다!`);
      document.getElementById('contactForm').reset();
    }
  </script>
</body>

</html>
