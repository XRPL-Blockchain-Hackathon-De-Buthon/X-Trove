X-Trove

개요
XRPL 테스트넷 기반 GUI 애플리케이션으로, Tkinter 또는 웹을 활용해 NFT 발행·전송, 에스크로 거래를 테스트합니다.

Standby와 Operational 계정 간 XRP·NFT 관리, QR 코드 생성 기능을 제공합니다.

주요 기능
계정 관리: Standby/Operational 계정 생성 및 조회
XRP 전송: 계정 간 XRP 이동
NFT 관리: 발행, 조회, 전송, QR 코드 생성
에스크로 관리: 생성, 완료, 취소
거래 내역: JSON 파일 저장 및 조회
요구 사항
Python 3.8+
사용법
Accounts & NFTs
계정 생성: "Get Standby/Operational Account"
정보 조회: "Get Standby/Op Account Info"
XRP 전송: "Send XRP >" 또는 "< Send XRP"
NFT 발행: URI 등 입력 후 "Mint NFT"
NFT 조회: "Get NFTs"
NFT 전송: NFT ID 입력 후 "Transfer NFT >"
QR 코드: "Generate QR Code"
거래 내역: "View History"
Escrow
생성: Seed, Amount 등 입력 후 "Create Escrow"
완료: Seed, Owner 등 입력 후 "Finish Escrow"
취소: Seed, Owner 등 입력 후 "Cancel Escrow"
결과
텍스트 박스에 JSON 출력, 오류 시 "Error: ..." 표시
작성자
김현우
유승기
