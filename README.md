ReadMe

X-Trove

[개요]

  XRPL 테스트넷 기반 GUI 애플리케이션으로, Tkinter를 활용해 NFT 발행·전송, 에스크로 거래를 테스트합니다.
  
  Standby와 Operational 계정 간 XRP·NFT 관리와 QR 코드 생성 기능을 제공합니다.
  
  블록체인 기술을 직관적으로 테스트할 수 있는 환경을 목표로 개발되었습니다.

[주요 기능]

  계정 관리 Standby/Operational 계정 생성 및 정보 조회 계정 시드와 주소 관리 XRP 전송
  
  두 계정 간 XRP 송금 기능 잔액 확인 및 수수료 처리 NFT 관리
  
  NFT 발행(Mint), 조회(Get), 전송(Transfer) QR 코드를 통한 NFT 정보 시각화 에스크로 관리
  
  에스크로 생성(Create), 완료(Finish), 취소(Cancel) 조건 기반 안전 거래 지원 거래 내역
  
  JSON 파일에 거래 기록 저장 과거 거래 내역 조회 기능 요구 사항
  
  Python 3.8+ 필요 라이브러리: tkinter (GUI) xrpl-py (XRPL 통신) qrcode (QR 코드 생성) pillow (이미지 처리) 설치 명령어: pip install xrpl-py qrcode pillow 설치 방법
  
  리포지토리 클론 git clone cd X-Trove 라이브러리 설치 pip install -r requirements.txt 실행 python main.py 사용법

Accounts & NFTs 탭

  계정 생성: "Get Standby/Operational Account" 버튼 클릭 정보 조회: "Get Standby/Op Account Info"로 잔액 및 상세 정보 확인 XRP 전송: "Send XRP >" 또는 "< Send XRP"로 계정 간 이동 NFT 발행: URI, Flags 등 입력 후 "Mint NFT" 클릭 NFT 조회: "Get NFTs"로 보유 NFT 목록 확인 NFT 전송: NFT ID 입력 후 "Transfer NFT >" 실행 QR 코드 생성: "Generate QR Code"로 NFT 정보 표시 거래 내역: "View History"로 기록 조회 Escrow 탭
  
  생성: Seed, Amount, Destination 등 입력 후 "Create Escrow" 완료: Seed, Owner, Offer Sequence 입력 후 "Finish Escrow" 취소: Seed, Owner, Offer Sequence 입력 후 "Cancel Escrow" 결과 확인
  
  작업 결과는 텍스트 박스에 JSON 형식으로 출력 오류 발생 시 "Error: ..." 메시지 표시 프로젝트 구조
  
  X-Trove/
  
  main.py 메인 애플리케이션 코드 data/ 거래 내역 및 QR 코드 저장 폴더 transactions.json 거래 기록 JSON 파일 nft_qr.png 생성된 QR 코드 이미지 modules/ XRPL 관련 모듈 (account.py, nft_mint.py 등) README.md 이 문서 주의 사항
  
  python package install :
   pip install Flask==2.3.3 Flask-CORS==4.0.0 qrcode==7.4.2 xrpl-py==2.2.0
  
  react project setup
   Install Dependencies: npm install
   Environment Variables Create a .env file in the frontend directory: REACT_APP_API_URL=http://localhost:5000/api
   Run the Development Server: npm start
  
  테스트넷: XRPL 테스트넷(https://s.devnet.rippletest.net:51234/) 사용 잔액: 최소 예비금 10 XRP와 수수료(10 drops) 필요 QR 코드: 로컬 URL(http://localhost:5000/nft) 기반, 배포 시 수정 필요

작성자 김현우 유승기
