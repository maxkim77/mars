# mars

문제:
React 프로젝트에서 페이지네이션 기능을 구현하는 과정에서 URL을 사용하여 페이지 번호를 관리하려고 했습니다. 그러나 useHistory를 사용하여 URL을 업데이트하는 부분에서 문제가 발생하여 페이지가 올바르게 렌더링되지 않았습니다.

원인:
useHistory는 react-router-dom v5에서 사용되는 훅으로, 최신 버전인 react-router-dom v6에서는 useNavigate로 대체되었습니다. 따라서 useHistory를 사용하여 URL을 업데이트하려고 할 때 발생한 호환성 문제였습니다.

해결 방법:
react-router-dom v6에서 제공하는 useNavigate 훅을 사용하여 URL을 업데이트하도록 코드를 수정했습니다.
useHistory를 useNavigate로 변경하고, history.push 대신 navigate를 사용하여 URL을 업데이트했습니다.
최종 코드:
