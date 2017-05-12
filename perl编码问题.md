# perl编码问题

中文乱码大多是由于编码格式错误引起的。

我们使用perl可以使用两个包来完成转码的操作。

```perl
use Encode;
use Encode::Guess;

sub enc_gb2312($) {
	my $data = shift;
      my $enc = guess_encoding($data, qw/utf8 gbk gb2312 big5/);
      ref($enc) or die "Can't guess: $enc"; # trap error this way
      my $rel = decode($enc->name, $data);
      $rel = Encode::encode("gb2312", $rel);
      return $rel;
}
```

