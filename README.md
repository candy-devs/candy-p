# candy-p

`CANDY`

## DBModeling

```
MySQL
ArticleBody; ArticleId, Title, WriteTime, ~Author, Body, ~BucketId, UpVote, DownVote, Etc
User(Author); UserId, NickName, Id, Password, AssignTime, LastLoginTime, LastPasswordChangeTime
Bucket; BucketId, ~Gift, MaxSize, CurrentSize
Gift; GiftId, ~UserId, ~BucketId, NumberOfCredit, ~TransferId
TransferTracker; TransferId, TransferType ~FromTo, ~UserId, ~WhereTo, ~BucketId, ~ToUserId, NumberOfCredit, @StoreProofHashCode, @ReciptId
    => TransferType; root => user, user => user, user => bucket, bucket => user
```

## 기능 구현

### 게시글의 작성 및 조회, 수정, 삭제, 신고

### 선물하기, 후원하기 기능 구현

