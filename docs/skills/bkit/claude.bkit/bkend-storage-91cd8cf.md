# bkend-storage

## 요약

bkend.ai file storage expert skill. Covers single/multiple/multipart file upload via Presigned URL, file download (CDN vs Presigned), 4 visibility levels (public/private/protected/shared), bucket management, and file metadata. Triggers: file upload, download, presigned, bucket, storage, CDN, image, 파일 업로드, 다운로드, 버킷, 스토리지, 이미지, ファイルアップロード, ダウンロード, バケット, ストレージ, 文件上传, 下载, 存储桶, 存储, carga de archivos, descarga, almacenamiento, cubo, telechargement, televersement, stockage, seau, Datei-Upload, Download, Speicher, Bucket, caricamento file, scaricamento, archiviazione, bucket Do NOT use for: database operations (use bkend-data), authentication (use bkend-auth).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/bkend-storage/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/bkend-storage-91cd8cf.md` |
| 사용자 호출 | false |

## 언제 쓰나

bkend.ai file storage expert skill. Covers single/multiple/multipart file upload via Presigned URL, file download (CDN vs Presigned), 4 visibility levels (public/private/protected/shared), bucket management, and file metadata. Triggers: file upload, download, presigned, bucket, storage, CDN, image, 파일 업로드, 다운로드, 버킷, 스토리지, 이미지, ファイルアップロード, ダウンロード, バケット, ストレージ, 文件上传, 下载, 存储桶, 存储, carga de archivos, descarga, almacenamiento, cubo, telechargement, televersement, stockage, seau, Datei-Upload, Download, Speicher, Bucket, caricamento file, scaricamento, archiviazione, bucket Do NOT use for: database operations (use bkend-data), authentication (use bkend-auth).

## 주요 내용

- **진행 방식**: bkend MCP does NOT have dedicated storage tools. Use this workflow: **Search docs**: `search_docs` with query "file upload presigned url" **Get examples**: `search_docs` with query "file upload code examples" **Generate code**: AI generates REST API code for file operations Searchable Storage Docs

## 원본 문서 구조

- Upload Methods
- Presigned URL
- File Visibility (4 levels)
- Size Limits
- Storage Categories
- MCP Storage Workflow
  - Searchable Storage Docs
- REST Storage API
- Multipart Upload (Large Files)
- Upload Flow (Single File)
- Multipart Upload Flow (Large File)
- Official Documentation (Live Reference)

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/bkend-storage/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.
