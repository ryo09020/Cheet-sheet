# gitのエラー集
1. ローカルのコミット履歴と、リモートのコミット履歴が同一でない
強制的にプッシュする方法
'''
git push -f -u origin master
'''
リモートのorigin/masterにローカルのmasterをpush -fはforse, -uはupsteam「upstream（上流）ブランチを追跡する」
