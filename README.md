# Dify 채팅형 웹 앱 템플릿

- 한국어 지원 추가
- powered by 제거
- 기본 privacy 페이지 레이아웃
-

이 프로젝트는 [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app)으로 부트스트랩된 [Next.js](https://nextjs.org/) 프로젝트입니다.

## 앱 설정

현재 디렉토리에 `.env.local` 파일을 생성하고 `.env.example`의 내용을 복사하여 다음 내용을 설정하세요:

```
# APP ID: 앱의 고유 식별자입니다. 앱 상세 페이지 URL에서 찾을 수 있습니다.
# 예를 들어, URL `https://cloud.dify.ai/app/xxx/workflow`에서 `xxx` 값이 APP ID입니다.
NEXT_PUBLIC_APP_ID=

# APP API Key: 앱의 API 요청을 인증하는 데 사용되는 키입니다.
# 앱의 "API Access" 페이지에서 우측 상단의 "API Key" 버튼을 클릭하여 생성할 수 있습니다.
NEXT_PUBLIC_APP_KEY=

# APP URL: API의 기본 URL입니다. Dify 클라우드 서비스를 사용하는 경우, 다음으로 설정하세요: https://api.dify.ai/v1
NEXT_PUBLIC_API_URL=
```

`config/index.ts` 파일에서 추가 설정을 할 수 있습니다:

```js
export const APP_INFO: AppInfo = {
  title: "채팅 앱",
  description: "",
  copyright: "",
  privacy_policy: "",
  default_language: "ko",
};

export const isShowPrompt = true;
export const promptTemplate = "";
```

## 시작하기

먼저 의존성을 설치하세요:

```bash
npm install
# 또는
yarn
# 또는
pnpm install
```

그 다음, 개발 서버를 실행하세요:

```bash
npm run dev
# 또는
yarn dev
# 또는
pnpm dev
```

브라우저에서 [http://localhost:3000](http://localhost:3000)을 열어 결과를 확인하세요.

## Docker 사용하기

```
docker build . -t <DOCKER_HUB_REPO>/webapp-conversation:latest
# 이제 3000번 포트에서 접근할 수 있습니다
docker run -p 3000:3000 <DOCKER_HUB_REPO>/webapp-conversation:latest
```

브라우저에서 [http://localhost:3000](http://localhost:3000)을 열어 결과를 확인하세요.

## 더 알아보기

Next.js에 대해 더 알아보려면 다음 자료를 참고하세요:

- [Next.js 문서](https://nextjs.org/docs) - Next.js 기능과 API에 대해 알아보세요.
- [Next.js 학습](https://nextjs.org/learn) - 대화형 Next.js 튜토리얼입니다.

[Next.js GitHub 저장소](https://github.com/vercel/next.js/)를 확인해보세요 - 피드백과 기여를 환영합니다!

## Vercel에 배포하기

> ⚠️ [Vercel Hobby](https://vercel.com/pricing)를 사용하는 경우, Vercel의 제한으로 인해 메시지가 잘릴 수 있습니다.

Next.js 앱을 배포하는 가장 쉬운 방법은 Next.js의 제작자인 [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme)을 사용하는 것입니다.

자세한 내용은 [Next.js 배포 문서](https://nextjs.org/docs/deployment)를 확인하세요.
