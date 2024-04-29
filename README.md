# quick-proj-midiadownload

web browser -> devtools -> console -> enter the command


``` log
// 현재 페이지의 모든 미디어 요소를 가져오는 함수
function getAllMediaElements() {
  return Array.from(document.querySelectorAll('video, audio'));
}

// 미디어 요소를 새 탭에서 열어주는 함수
function openMediaInNewTab(mediaElement) {
  if (!mediaElement.src) {
    console.error('Media element has no source.');
    return;
  }

  // 새 탭을 열고 미디어 리소스를 로드
  window.open(mediaElement.src, '_blank');
}

// 모든 미디어 요소를 가져와서 새 탭에서 열기
getAllMediaElements().forEach(openMediaInNewTab);
```
